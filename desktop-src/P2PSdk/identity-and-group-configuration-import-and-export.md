---
description: È possibile importare ed esportare i file di configurazione delle identità e dei gruppi di peer da un endpoint a un altro usando le funzioni di importazione ed esportazione di identità disponibili in Identity Manager e le API di raggruppamento.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importazione ed esportazione della configurazione dell'identità e del gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756602"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importazione ed esportazione della configurazione dell'identità e del gruppo

È possibile importare ed esportare i file di configurazione delle identità e dei gruppi di peer da un endpoint a un altro usando le funzioni di importazione ed esportazione di identità disponibili in Identity Manager e le API di raggruppamento. Queste funzioni sono utili perché consentono a un utente di esportare in modo rapido e conveniente le identità e le informazioni di configurazione di gruppo da un computer a un altro computer.

## <a name="importing-and-exporting-peer-identity-data"></a>Importazione ed esportazione di dati di identità peer

I dati di identità di un peer vengono esportati chiamando [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) con il nome di identità da esportare e una password usata per crittografare le credenziali associate. Questa funzione restituisce una stringa XML che contiene il nome identità del peer e le credenziali crittografate per l'identità specifica, che può quindi essere passata a un altro computer utilizzando un meccanismo di trasferimento esterno, ad esempio un messaggio di posta elettronica. Nell'esempio seguente viene illustrato il formato della stringa XML:

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

È possibile recuperare i dati di identità esportati chiamando [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)e passando la stringa XML con la password fornita nella chiamata precedente a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport). Questa funzione restituisce il nome peer dell'identità importata. Il nome dell'identità importato e le credenziali possono essere usati esattamente come un nome di identità restituito da [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) o [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

> [!Note]  
> Quando si chiama [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), l'utente dell'applicazione o dell'API deve fornire una password complessa di lunghezza sufficiente. Questo è importante perché i dati di identità importati contengono la chiave privata per l'identità.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importazione ed esportazione di una configurazione di identità di gruppo

Il raggruppamento peer consente a un peer di esportare i dati di configurazione del gruppo da un endpoint a un altro usando API di importazione ed esportazione specifiche. Per importare i dati di configurazione, è necessario che l'identità del peer che esegue l'importazione (e che in precedenza ha eseguito l'esportazione) sia presente nel computer in cui devono essere importati i dati di configurazione. Questa identità può essere ottenuta tramite l'esportazione e l'importazione mediante i metodi specificati nella sezione precedente di questo argomento: [importazione ed esportazione di dati di identità peer](#importing-and-exporting-peer-identity-data).

I dati di configurazione del gruppo contengono tutte le informazioni per un'identità per l'aggiunta a un gruppo da un nuovo endpoint. In particolare, i dati di configurazione contengono la catena di GMC, il nome del peer del gruppo, il nome del cloud, l'ambito e un set di flag specifici PNRP. Per un'identità proprietaria di un gruppo, una chiave privata per il gruppo viene inclusa nelle informazioni di configurazione del gruppo.

> [!Note]  
> Quando si chiama [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), un'applicazione o un utente dell'API deve fornire una password complessa di lunghezza sufficiente. Questo è importante perché i dati di identità importati contengono la chiave privata per il gruppo.

 

Per esportare la configurazione del gruppo peer corrente, chiamare [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passando l'handle al gruppo (ottenuto da una chiamata precedente a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)o [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) e una password usata per crittografare e proteggere il file di configurazione. Questa funzione restituisce una stringa XML che contiene la configurazione nel formato dell'esempio seguente, che può quindi essere scritto in un file e passato a un altro computer tramite un meccanismo di trasferimento esterno, ad esempio un messaggio di posta elettronica.

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

Dopo aver ottenuto la configurazione di gruppo come stringa XML, è possibile importare il gruppo chiamando [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) con la stringa XML di configurazione e la password specifica fornita a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig). Questa funzione restituisce un nome di identità e un nome peer di gruppo, che può quindi essere fornito a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e una connessione al gruppo stabilita.

 

 



