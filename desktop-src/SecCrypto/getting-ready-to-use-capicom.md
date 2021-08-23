---
description: Le applicazioni che usano oggetti CAPICOM devono essere create usando CAPICOM.dll. CAPICOM.dll essere presenti e registrati in fase di esecuzione per usare gli oggetti CAPICOM.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Introduzione all'uso di CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a6b76c293395fd0979cf5c304b27bae75622996279bd891b8c0c1301dca82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006630"
---
# <a name="getting-ready-to-use-capicom"></a>Introduzione all'uso di CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Le applicazioni che usano oggetti CAPICOM devono essere create usando CAPICOM.dll. CAPICOM.dll essere presenti e registrati in fase di esecuzione per usare gli oggetti CAPICOM. CAPICOM.dll devono essere aggiunti ai riferimenti Visual Basic progetti per l'uso di oggetti CAPICOM.

CAPICOM è disponibile come file ridistribuibile che può essere scaricato da [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281). Per informazioni sulle versioni capiCOM, vedere [CapiCOM Versions](capicom-versions.md).

**Per registrare CAPICOM.dll**

-   Al prompt dei comandi modificare la directory nella directory in cui CAPICOM.dll e quindi immettere il comando seguente:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Limitazioni del codice di esempio

Per fornire codice più conciso e leggibile, i principi di buona pratica di programmazione non sono sempre seguiti in questi esempi. In particolare, vengono visualizzate solo risposte di errore limitate. Le applicazioni funzionanti devono sempre controllare i codici di errore restituiti ed eseguire le azioni appropriate quando viene rilevato un errore.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Contenitori di chiavi, chiavi e certificati necessari in CAPICOM

Anche se alcune operazioni con oggetti CAPICOM possono essere [](../secgloss/d-gly.md) eseguite in qualsiasi computer da qualsiasi utente, la creazione di firme digitali e il recupero del contenuto non crittografato di un messaggio in busta tramite oggetti CAPICOM sono operazioni basate su certificati. L'utente che crea una firma digitale e l'utente che recupera il contenuto crittografato di un messaggio in busta devono avere un certificato digitale con una chiave privata associata disponibile. Se non è presente un certificato con una chiave privata associata, l'operazione di crittografia avrà esito negativo. Gli utenti delle applicazioni CAPICOM devono assicurarsi di avere il certificato appropriato e la chiave privata disponibile quando le applicazioni sono in esecuzione.

Alcuni esempi nelle sezioni seguenti eseguono operazioni che richiedono una coppia di chiavi [*pubblica/privata*](../secgloss/p-gly.md) disponibile per la crittografia e la decrittografia di file, messaggi e firme. Molti di questi programmi verranno compilati ed eseguiti ma avranno esito negativo in fase di esecuzione senza l'esistenza di contenitori di [*chiavi,*](../secgloss/k-gly.md)chiavi, archivi certificati e [*certificati*](../secgloss/c-gly.md) in tali archivi.

**Per creare un certificato autofirmato**

1.  Installare gli strumenti di firma. Vengono installati come parte di Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK) o .NET Framework SDK.
2.  Dopo Makecert.exe scaricato, eseguire il comando seguente al prompt dei comandi, sostituendo un nome utente con *UserName*, un nome dell'organizzazione per *OrganizationName* e un nome società per *CompanyName*:

    **makecert -r -n "cn=**_UserName_*_, ou=_*_OrganizationName_*_, o=_*_CompanyName_*_" -ss my_*

3.  Il certificato può essere inserito nell'archivio My dell'utente corrente. Importare il certificato creato nell'archivio radice in modo che sia attendibile.

 

 
