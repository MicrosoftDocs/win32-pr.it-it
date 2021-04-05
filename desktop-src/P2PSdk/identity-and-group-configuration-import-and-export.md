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
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="2c9f1-103">Importazione ed esportazione della configurazione dell'identità e del gruppo</span><span class="sxs-lookup"><span data-stu-id="2c9f1-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="2c9f1-104">È possibile importare ed esportare i file di configurazione delle identità e dei gruppi di peer da un endpoint a un altro usando le funzioni di importazione ed esportazione di identità disponibili in Identity Manager e le API di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="2c9f1-105">Queste funzioni sono utili perché consentono a un utente di esportare in modo rapido e conveniente le identità e le informazioni di configurazione di gruppo da un computer a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="2c9f1-106">Importazione ed esportazione di dati di identità peer</span><span class="sxs-lookup"><span data-stu-id="2c9f1-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="2c9f1-107">I dati di identità di un peer vengono esportati chiamando [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) con il nome di identità da esportare e una password usata per crittografare le credenziali associate.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="2c9f1-108">Questa funzione restituisce una stringa XML che contiene il nome identità del peer e le credenziali crittografate per l'identità specifica, che può quindi essere passata a un altro computer utilizzando un meccanismo di trasferimento esterno, ad esempio un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="2c9f1-109">Nell'esempio seguente viene illustrato il formato della stringa XML:</span><span class="sxs-lookup"><span data-stu-id="2c9f1-109">The following example shows you the format of the XML string:</span></span>

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

<span data-ttu-id="2c9f1-110">È possibile recuperare i dati di identità esportati chiamando [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)e passando la stringa XML con la password fornita nella chiamata precedente a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span><span class="sxs-lookup"><span data-stu-id="2c9f1-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="2c9f1-111">Questa funzione restituisce il nome peer dell'identità importata.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="2c9f1-112">Il nome dell'identità importato e le credenziali possono essere usati esattamente come un nome di identità restituito da [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) o [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="2c9f1-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="2c9f1-113">Quando si chiama [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), l'utente dell'applicazione o dell'API deve fornire una password complessa di lunghezza sufficiente.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="2c9f1-114">Questo è importante perché i dati di identità importati contengono la chiave privata per l'identità.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="2c9f1-115">Importazione ed esportazione di una configurazione di identità di gruppo</span><span class="sxs-lookup"><span data-stu-id="2c9f1-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="2c9f1-116">Il raggruppamento peer consente a un peer di esportare i dati di configurazione del gruppo da un endpoint a un altro usando API di importazione ed esportazione specifiche.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="2c9f1-117">Per importare i dati di configurazione, è necessario che l'identità del peer che esegue l'importazione (e che in precedenza ha eseguito l'esportazione) sia presente nel computer in cui devono essere importati i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="2c9f1-118">Questa identità può essere ottenuta tramite l'esportazione e l'importazione mediante i metodi specificati nella sezione precedente di questo argomento: [importazione ed esportazione di dati di identità peer](#importing-and-exporting-peer-identity-data).</span><span class="sxs-lookup"><span data-stu-id="2c9f1-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="2c9f1-119">I dati di configurazione del gruppo contengono tutte le informazioni per un'identità per l'aggiunta a un gruppo da un nuovo endpoint.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="2c9f1-120">In particolare, i dati di configurazione contengono la catena di GMC, il nome del peer del gruppo, il nome del cloud, l'ambito e un set di flag specifici PNRP.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="2c9f1-121">Per un'identità proprietaria di un gruppo, una chiave privata per il gruppo viene inclusa nelle informazioni di configurazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="2c9f1-122">Quando si chiama [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), un'applicazione o un utente dell'API deve fornire una password complessa di lunghezza sufficiente.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="2c9f1-123">Questo è importante perché i dati di identità importati contengono la chiave privata per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="2c9f1-124">Per esportare la configurazione del gruppo peer corrente, chiamare [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passando l'handle al gruppo (ottenuto da una chiamata precedente a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)o [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) e una password usata per crittografare e proteggere il file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="2c9f1-125">Questa funzione restituisce una stringa XML che contiene la configurazione nel formato dell'esempio seguente, che può quindi essere scritto in un file e passato a un altro computer tramite un meccanismo di trasferimento esterno, ad esempio un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

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

<span data-ttu-id="2c9f1-126">Dopo aver ottenuto la configurazione di gruppo come stringa XML, è possibile importare il gruppo chiamando [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) con la stringa XML di configurazione e la password specifica fornita a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span><span class="sxs-lookup"><span data-stu-id="2c9f1-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="2c9f1-127">Questa funzione restituisce un nome di identità e un nome peer di gruppo, che può quindi essere fornito a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e una connessione al gruppo stabilita.</span><span class="sxs-lookup"><span data-stu-id="2c9f1-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



