---
description: È possibile specificare un descrittore di sicurezza per una pipe anonima quando si chiama la funzione non. Il descrittore di sicurezza controlla l'accesso alle estremità di lettura e scrittura della pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Diritti di accesso e sicurezza per le pipe anonime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318075"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Diritti di accesso e sicurezza per le pipe anonime

La sicurezza di Windows consente di controllare l'accesso alle pipe anonime. Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per una pipe quando si chiama la funzione [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) . Il descrittore di sicurezza controlla l'accesso alle estremità di lettura e scrittura della pipe. Se si specifica **null**, la pipe ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per una pipe provengono dal token primario o di rappresentazione del creatore.

Per recuperare il descrittore di sicurezza di una pipe, chiamare la funzione [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Per modificare il descrittore di sicurezza di una pipe, chiamare la funzione [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

La funzione [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) restituisce due handle alla pipe anonima: un handle di lettura con \_ accesso generico Read e Synchronize e un handle di scrittura con \_ accesso generico di scrittura e sincronizzazione. \_ \_ L'accesso di lettura e scrittura generico usa lo stesso mapping dei diritti di accesso per le named pipe.

L' \_ accesso in lettura generico per una pipe anonima combina i diritti per la lettura dei dati dalla pipe, la lettura degli attributi della pipe, la lettura degli attributi estesi e la lettura dell'elenco DACL della pipe.

L' \_ accesso in scrittura generico per una pipe anonima combina i diritti per la scrittura dei dati nella pipe, l'aggiunta di dati, la scrittura di attributi pipe, la scrittura di attributi estesi e la lettura dell'elenco DACL della pipe.

 

 
