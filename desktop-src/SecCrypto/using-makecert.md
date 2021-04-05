---
description: Usare i comandi MakeCert per creare certificati di test usando le opzioni disponibili con Internet Explorer versione 4,0 o successiva.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Uso di MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753447"
---
# <a name="using-makecert"></a>Uso di MakeCert

Negli esempi seguenti vengono utilizzati i comandi [Makecert](makecert.md) per creare certificati di test utilizzando le opzioni disponibili con Internet Explorer versione 4,0 o successiva.

-   Creare un certificato emesso dalla radice di test predefinita. Salvare il certificato in un file.

    **Makecert** *MyNew. cer*

-   Creare un certificato emesso dalla radice di test predefinita. Salvarlo in un archivio certificati.

    **Makecert-SS** *MyNewStore*

-   Creare un certificato emesso dalla radice di test predefinita. Creare un contenitore di chiavi e salvare il certificato in un archivio e in un file.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*

-   Creare un certificato emesso dalla radice di test predefinita. Creare un file di chiave privata e salvare il certificato in un archivio e in un file.

    **Makecert-SV** *MyKeyFile* **-SS** *MyNewStore* *MyNew. cer*

-   Creare un certificato emesso dalla radice di test predefinita. Creare un contenitore di chiavi, salvare il certificato in un archivio e in un file e rendere esportabile la chiave privata.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**

-   Creare un certificato usando la radice di test predefinita. Salvare il certificato in un archivio. Quindi, creare un altro certificato emesso dal certificato appena creato. Salvare il secondo certificato in un altro archivio.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* **Makecert-is** *MyNewStore* **-SS** *AnotherStore*

-   Creare un certificato usando la radice di test predefinita. Salvare il certificato nell'archivio personale. Quindi creare un altro certificato usando il certificato appena creato. Se è presente più di un certificato nell'archivio MY, il certificato deve essere identificato con il nome comune.

    **Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My Makecert-is My-in "XXZZYY"-SS** *AnotherStore*

-   Creare un certificato usando la radice di test predefinita. Salvare il certificato nell'archivio personale e in un file. Quindi creare un altro certificato usando il certificato *MyNew* appena creato. Se è presente più di un certificato nell'archivio MY, identificare in modo univoco il primo certificato usando il nome del file del certificato.

    **Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My** *MyNew. cer* **Makecert-is my-IC** *MyNew. cer* **-SS** *AnotherStore*

 

 



