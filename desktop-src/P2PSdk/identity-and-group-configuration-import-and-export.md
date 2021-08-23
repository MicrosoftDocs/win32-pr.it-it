---
description: I file di configurazione di identità e gruppi peer possono essere importati ed esportati da un endpoint a un altro usando le funzioni di importazione ed esportazione delle identità disponibili nelle API Identity Manager e Grouping.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importazione ed esportazione della configurazione di identità e gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0102bda821b7157edc512aeea4a8e315c0dbfa1def85f9a61919ec0f2c86da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519331"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importazione ed esportazione della configurazione di identità e gruppi

I file di configurazione di identità e gruppi peer possono essere importati ed esportati da un endpoint a un altro usando le funzioni di importazione ed esportazione delle identità disponibili nelle API Identity Manager e Grouping. Queste funzioni sono utili perché consentono a un utente di esportare in modo rapido e pratico le identità e le informazioni di configurazione del gruppo da un computer a un altro computer.

## <a name="importing-and-exporting-peer-identity-data"></a>Importazione ed esportazione di dati di identità peer

I dati di identità di un peer vengono esportati chiamando [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) con il nome dell'identità da esportare e una password usata per crittografare le credenziali associate. Questa funzione restituisce una stringa XML che contiene il nome dell'identità del peer e le credenziali crittografate per tale identità specifica, che possono quindi essere passate a un computer diverso usando un meccanismo di trasferimento esterno, ad esempio la posta elettronica. L'esempio seguente illustra il formato della stringa XML:

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

I dati di identità esportati possono essere recuperati chiamando [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)e passando la stringa XML con la password specificata nella chiamata precedente a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport). Questa funzione restituisce il nome peer dell'identità importata. Il nome e le credenziali dell'identità importati possono essere usati esattamente come un nome di identità restituito da [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) [**o PeerIdentityCreate.**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)

> [!Note]  
> Quando si chiama [**PeerIdentityExport,**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)l'utente dell'applicazione o dell'API deve fornire una password complessa di lunghezza sufficiente. Questo è importante perché i dati di identità importati contengono la chiave privata per l'identità.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importazione ed esportazione di una configurazione dell'identità del gruppo

Il raggruppamento peer consente a un peer di esportare i dati di configurazione del gruppo da un endpoint a un altro usando API di importazione ed esportazione specifiche. Per importare i dati di configurazione, l'identità del peer che esegue l'importazione (e chi ha eseguito in precedenza l'esportazione) deve essere presente nel computer in cui devono essere importati i dati di configurazione. Questa identità può essere ottenuta esportando e importando l'identità tramite i metodi specificati nella sezione precedente di questo argomento: Importazione ed esportazione di dati di [identità peer](#importing-and-exporting-peer-identity-data).

I dati di configurazione del gruppo contengono tutte le informazioni che un'identità deve aggiungere a un gruppo da un nuovo endpoint. In particolare, i dati di configurazione contengono la catena GMC, il nome peer del gruppo, il nome cloud, l'ambito e un set di flag specifici PNRP. Per un'identità proprietaria di un gruppo, nelle informazioni di configurazione del gruppo viene inclusa una chiave privata per il gruppo.

> [!Note]  
> Quando si chiama [**PeerGroupExportConfig,**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)un utente dell'applicazione o dell'API deve fornire una password complessa di lunghezza sufficiente. Questo è importante perché i dati di identità importati contengono la chiave privata per il gruppo.

 

Per esportare la configurazione del gruppo peer corrente, chiamare [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passando l'handle al gruppo (ottenuto da una chiamata precedente a [**PeerGroupJoin,**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)o [**PeerGroupCreate)**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)e una password usata per crittografare e proteggere il file di configurazione. Questa funzione restituisce una stringa XML che contiene la configurazione nel formato dell'esempio seguente, che può quindi essere scritta in un file e passata a un altro computer usando un meccanismo di trasferimento esterno, ad esempio la posta elettronica.

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

Dopo aver ottenuto la configurazione del gruppo come stringa XML, il gruppo può essere importato chiamando [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) con la stringa XML di configurazione e la password specifica fornita a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig). Questa funzione restituisce un nome di identità e un nome peer del gruppo, che possono quindi essere forniti a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e una connessione al gruppo stabilita.

 

 



