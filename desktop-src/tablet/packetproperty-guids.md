---
description: Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti usati dalla struttura PACKET \_ PROPERTY.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c897e19aea30db6e5dfa026fbdcfec77de5afa4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481647"
---
# <a name="packetproperty-guids"></a>GUID PacketProperty

Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti usati dalla [**struttura PACKET \_ PROPERTY.**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)




| GUID | Descrizione | 
|------|-------------|
| GUID_ALTITUDE_ORIENTATION<br /> | Angolo tra l'asse della penna e la superficie del tablet. Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie. I valori sono negativi quando la penna viene invertita.<br /> | 
| GUID_AZIMUTH_ORIENTATION<br /> | Rotazione in senso orario del cursore intorno all'asse z attraverso un intervallo circolare completo.<br /> | 
| GUID_BOXNUMBER<br /> | GUID utilizzato per recuperare il numero di casella per un'alternativa di riconoscimento input penna quando il riconoscimento funziona in modalità box.<br /> | 
| GUID_BUTTON_PRESSURE<br /> | Pressione su un pulsante sensibile alla pressione.<br /> | 
| GUID_NORMAL_PRESSURE<br /> | GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna perpendicolare alla superficie del tablet. Maggiore è la pressione sulla punta della penna, maggiore sarà l'input penna disegnato.<br /> | 
| GUID_PACKET_STATUS<br /> | Contiene uno o più dei valori flag seguenti:<br /><ul><li>Il cursore tocca la superficie di disegno (Valore = 1).</li><li>Il cursore viene invertito. Ad esempio, l'estremità della gomma della penna punta verso la superficie (Valore = 2).</li><li>Non usato (Valore = 4).</li><li>Viene premuto il pulsante a sospensione (Valore = 8).</li></ul> | 
| GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br /> | Identificatore del contatto del dispositivo per un pacchetto.<br /> | 
| GUID_SERIAL_NUMBER<br /> | Identifica il pacchetto. Si tratta dello stesso valore utilizzato per recuperare il pacchetto dalla coda di pacchetti.<br /> | 
| GUID_TANGENT_PRESSURE<br /> | GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna lungo il piano della superficie del tablet.<br /> | 
| GUID_TIMER_TICK<br /> | Ora in cui è stato generato il pacchetto.<br /> | 
| GUID_TWIST_ORIENTATION<br /> | Rotazione in senso orario del cursore intorno al proprio asse.<br /> | 
| GUID_X<br /> | Coordinata x nello spazio delle coordinate della compressa. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br /> | 
| GUID_X_TILT_ORIENTATION<br /> | Per un cursore penna, l'orientamento dell'inclinazione x è l'angolo tra il piano y, z e il piano della penna e dell'asse y. Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna si trova a destra della perpendicolare.<br /> | 
| GUID_Y<br /> | Coordinata y nello spazio delle coordinate della compressa. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br /> | 
| GUID_Y_TILT_ORIENTATION<br /> | Per un cursore penna, l'orientamento dell'inclinazione y è l'angolo tra il piano x, z e il piano della penna e dell'asse x. Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o lontano dall'utente.<br /> | 
| GUID_Z<br /> | Coordinata z o distanza della punta della penna dalla superficie del tablet. Il <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> di enumerazione determina l'unità di misura per questa proprietà. <br /> | 




 

> [!Note]  
> Il campo TangentPressure rappresenta la pressione lungo il piano della superficie del tablet; Il campo NormalPressure rappresenta la pressione perpendicolare al piano della superficie della compressa.

 

 

 




