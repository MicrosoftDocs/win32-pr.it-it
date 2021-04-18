---
description: Le applicazioni che utilizzano oggetti CAPICOM devono essere create utilizzando CAPICOM.dll. Per usare gli oggetti CAPICOM, è inoltre necessario che il CAPICOM.dll sia presente e registrato in fase di esecuzione.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Preparazione all'uso di CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316169"
---
# <a name="getting-ready-to-use-capicom"></a>Preparazione all'uso di CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Le applicazioni che utilizzano oggetti CAPICOM devono essere create utilizzando CAPICOM.dll. Per usare gli oggetti CAPICOM, è inoltre necessario che il CAPICOM.dll sia presente e registrato in fase di esecuzione. È necessario aggiungere CAPICOM.dll ai riferimenti ai progetti Visual Basic per usare oggetti CAPICOM.

CAPICOM è disponibile come file ridistribuibile che può essere scaricato da [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281). Per informazioni sulle versioni di CAPICOM, vedere [versioni di CAPICOM](capicom-versions.md).

**Per registrare CAPICOM.dll**

-   Al prompt dei comandi, passare alla directory in cui è archiviato CAPICOM.dll, quindi immettere il comando seguente:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Limitazioni del codice di esempio

Per fornire codice più conciso e leggibile, i principi delle procedure di programmazione valide non sono sempre seguiti in questi esempi. In particolare, vengono visualizzate solo le risposte di errore limitate. Le applicazioni in funzione devono sempre controllare i codici di errore restituiti ed eseguire le azioni appropriate quando viene rilevato un errore.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Contenitori chiave, chiavi e certificati necessari in CAPICOM

Mentre alcune operazioni con oggetti CAPICOM possono essere eseguite su qualsiasi computer da qualsiasi utente, la creazione di [*firme digitali*](../secgloss/d-gly.md) e il recupero del contenuto di testo non crittografato di un messaggio in busta con oggetti CAPICOM sono operazioni basate sui certificati. L'utente che crea una firma digitale e l'utente che recupera il contenuto crittografato di un messaggio in busta digitale deve disporre di un certificato digitale con una chiave privata associata disponibile. Se non è presente un certificato con una chiave privata associata, l'operazione di crittografia avrà esito negativo. Gli utenti di applicazioni CAPICOM devono assicurarsi che dispongano del certificato appropriato e della chiave privata disponibile quando le applicazioni sono in esecuzione.

Alcuni esempi nelle sezioni seguenti eseguono operazioni che richiedono una coppia di [*chiavi pubblica/privata*](../secgloss/p-gly.md) disponibile per la crittografia e la decrittografia di file, messaggi e firme. Molti di questi programmi verranno compilati ed eseguiti ma avranno esito negativo in fase di esecuzione senza la presenza di [*contenitori*](../secgloss/k-gly.md)di chiavi, chiavi, archivi certificati e [*certificati*](../secgloss/c-gly.md) appropriati in tali archivi.

**Per creare un certificato autofirmato**

1.  Installare gli strumenti di firma. Questi componenti vengono installati come parte di Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK) o SDK .NET Framework.
2.  Dopo aver scaricato Makecert.exe, eseguire il comando seguente al prompt dei comandi, sostituendo nome utente per nome *utente,* nome organizzazione per *OrganizationName* e nome della società per *CompanyName*:

    **makecert-r-n "CN =**_username_*_, ou =_*_OrganizationName_*_, o =_*_CompanyName_*_"-SS My_*

3.  Il certificato può essere inserito nell'archivio personale dell'utente corrente. Importare il certificato creato nell'archivio radice in modo che sia attendibile.

 

 
