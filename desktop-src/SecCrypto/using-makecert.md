---
description: Usare i comandi MakeCert per creare certificati di test usando le opzioni disponibili Internet Explorer versione 4.0 o successiva.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Uso di MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321eccfc26e3fc5bf13a541e1aab6a41b3f5d0930beed03f6033211bf63ac689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971551"
---
# <a name="using-makecert"></a>Uso di MakeCert

Gli esempi seguenti usano [i comandi MakeCert](makecert.md) per creare certificati di test usando le opzioni disponibili Internet Explorer versione 4.0 o successiva.

-   Creare un certificato emesso dalla radice di test predefinita. Salvare il certificato in un file.

    **MakeCert** *MyNew.cer*

-   Creare un certificato emesso dalla radice di test predefinita. Salvarlo in un archivio certificati.

    **MakeCert -ss** *MyNewStore*

-   Creare un certificato emesso dalla radice di test predefinita. Creare un contenitore di chiavi e salvare il certificato in un archivio e in un file.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*

-   Creare un certificato emesso dalla radice di test predefinita. Creare un file di chiave privata e salvare il certificato in un archivio e in un file.

    **MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*

-   Creare un certificato emesso dalla radice di test predefinita. Creare un contenitore di chiavi, salvare il certificato in un archivio e in un file e rendere esportabile la chiave privata.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**

-   Creare un certificato usando la radice di test predefinita. Salvare il certificato in un archivio. Creare quindi un altro certificato emesso dal certificato appena creato. Salvare il secondo certificato in un altro archivio.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*

-   Creare un certificato usando la radice di test predefinita. Salvare il certificato nell'archivio MY. Creare quindi un altro certificato usando il certificato appena creato. Se nell'archivio MY sono presenti più certificati, il certificato deve essere identificato usando il nome comune.

    **MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*

-   Creare un certificato usando la radice di test predefinita. Salvare il certificato nell'archivio MY e in un file. Creare quindi un altro certificato usando il certificato *MyNew* appena creato. Se nell'archivio MY sono presenti più certificati, identificare in modo univoco il primo certificato usando il nome file del certificato.

    **MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*

 

 



