---
description: È possibile specificare un descrittore di sicurezza per una pipe anonima quando si chiama la funzione CreatePipe. Il descrittore di sicurezza controlla l'accesso alle estremità di lettura e scrittura della pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Sicurezza della pipe anonima e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b54869584a70bfbe886740e979c44864d852de0df23e311eb4aad89c321662c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756358"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Sicurezza della pipe anonima e diritti di accesso

Windows sicurezza consente di controllare l'accesso alle pipe anonime. Per altre informazioni sulla sicurezza, vedere [Modello di controllo di accesso.](/windows/desktop/SecAuthZ/access-control-model)

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per una pipe quando si chiama la [**funzione CreatePipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) Il descrittore di sicurezza controlla l'accesso alle estremità di lettura e scrittura della pipe. Se si specifica **NULL,** la pipe ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per una pipe provengono dal token primario o di rappresentazione dell'autore.

Per recuperare il descrittore di sicurezza di una pipe, chiamare la [**funzione GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Per modificare il descrittore di sicurezza di una pipe, chiamare la [**funzione SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

La [**funzione CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) restituisce due handle alla pipe anonima: un handle di lettura con accesso READ e SYNCHRONIZE generici e un handle di scrittura con accesso WRITE e \_ SYNCHRONIZE \_ generici. \_L'accesso GENERIC READ e GENERIC WRITE usano lo stesso mapping dei diritti di accesso delle named \_ pipe.

L'accesso READ generico per una pipe anonima combina i diritti per leggere i dati dalla pipe, leggere gli attributi della pipe, leggere gli attributi estesi e leggere \_ l'elenco DACL della pipe.

L'accesso WRITE generico per una pipe anonima combina i diritti di scrittura dei dati nella pipe, l'aggiunta di dati, la scrittura di attributi della pipe, la scrittura di attributi estesi e la lettura \_ dell'elenco DACL della pipe.

 

 
