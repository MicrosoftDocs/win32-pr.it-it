---
title: Servizi di base TPM
description: Il software TPM fornisce servizi come API esposta tramite chiamata di procedura remota. Usare TPM per creare un modulo TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TPM Base Services TBS
- TPM Base Services TBS , home page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ccec7d7e70d8dece377518b379c0597c1392a3266222d6e70fa3ac524a010f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880462"
---
# <a name="tpm-base-services"></a>Servizi di base TPM

## <a name="purpose"></a>Scopo

La Trusted Platform Module (TPM) Base Services (TBS) consente di centralizzare l'accesso TPM tra le applicazioni.

La funzionalità TBS viene eseguita come servizio di sistema in Windows Server 2008, Windows Vista o sistemi operativi più nuovi. Fornisce servizi come API esposta tramite rpc (Remote Procedure Call). La funzionalità TBS usa le priorità specificate chiamando le applicazioni per pianificare in modo cooperativo l'accesso al TPM.

> [!Note]
>
> Il TPM può essere usato per le operazioni di archiviazione delle chiavi. Tuttavia, gli sviluppatori sono invitati a usare le [API Archiviazione chiave per](/windows/desktop/SecCNG/key-storage-and-retrieval) questi scenari. Le API key Archiviazione forniscono la funzionalità per creare, firmare o crittografare e rendere persistenti le chiavi crittografiche e sono di livello superiore e più facili da usare rispetto ai TBS per questi scenari di destinazione.

 

## <a name="developer-audience"></a>Sviluppatori

TbS è destinato all'uso da parte degli sviluppatori di applicazioni basate Windows sistemi operativi. Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di Windows Microsoft.

## <a name="run-time-requirements"></a>Requisiti di runtime

La funzionalità TBS richiede almeno Windows server 2008 o Windows Vista. Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [Informazioni sui TB](about-tbs.md)<br/>         | Concetti chiave e una visualizzazione di alto livello della funzionalità TBS.<br/>               |
| [Uso di TBS](using-tbs.md)<br/>         | Procedure e processi da tbs per l'uso dell'API TBS.<br/>                  |
| [Informazioni di riferimento su TBS](tbs-reference.md)<br/> | Documentazione sulle funzioni, le strutture e i codici restituiti da TBS.<br/> |



 

 

