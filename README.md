# Smart Home IoT Ontology (OWL 2)

## Scope
Models smart home entities: rooms, devices, sensors, observations, automation rules, users, notifications. Demonstrates OWL 2 DL reasoning with equivalent classes and inverse properties.

## Key Features (20 classes, 40+ properties)
- **Classes**: Home, Room, Device, Sensor, Actuator, Observation, AutomationRule, User, Notification, MonitoredRoom (inferred)...
- **Object Properties**: hasRoom, containsDevice↔locatedIn (inverse), makesObservation↔observedBy (inverse), hasRule, hasCondition, hasAction...
- **Data Properties**: deviceId (string), hasValue (decimal), observedAt (dateTime), ruleName (string)...

## Competency Questions (what the ontology answers)
1. Which rooms are monitored? → kitchen, livingRoom (inferred MonitoredRoom)
2. Which devices are sensors? → tempSensorKitchen (inferred Sensor)
3. What automation rules exist? → ruleMotionLight: "Turn on living room lamp..."
4. Which users own which devices? → alice ownsDevice tempSensorKitchen
5. What notifications were generated? → notif1 by ruleMotionLight

## Reasoning Demo (HermiT)
1. Open smarthome.owl in Protégé
2. Reasoner → HermiT → Start reasoner
3. **Classes tab**: See inferred hierarchy (Sensor under Device, MonitoredRoom under Room)
4. **Individuals**: tempSensorKitchen inferred as Sensor; kitchen inferred as MonitoredRoom
5. **Inverse properties**: tempSensorKitchen locatedIn kitchen (from containsDevice inverse)

## Deliverables
- `SmartHome.owl`: Main OWL 2 file

## Contacts
simone.dario@studenti.univr.it
