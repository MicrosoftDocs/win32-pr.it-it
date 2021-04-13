---
title: Servizi di base TPM
description: Il software TPM fornisce servizi come API esposte tramite Remote Procedure Call. Utilizzare TPM per creare un modulo TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- Servizi di base TPM TBS
- Servizi di base TPM TBS, home page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399390"
---
# <a name="tpm-base-services"></a>Servizi di base TPM

## <a name="purpose"></a>Scopo

La funzionalità dei servizi di base Trusted Platform Module (TPM) centralizza l'accesso TPM tra le applicazioni.

La funzionalità TBS viene eseguita come servizio di sistema in Windows Server 2008, Windows Vista o sistemi operativi più recenti. Fornisce servizi come API esposte tramite RPC (Remote Procedure Call). La funzionalità TBS usa le priorità specificate chiamando le applicazioni per pianificare in modo cooperativo l'accesso a TPM.

> [!Note]
>
> Il TPM può essere usato per le operazioni di archiviazione delle chiavi. Tuttavia, gli sviluppatori sono invitati a utilizzare le [API di archiviazione chiavi](/windows/desktop/SecCNG/key-storage-and-retrieval) per questi scenari. Le API di archiviazione chiavi forniscono la funzionalità per creare, firmare o crittografare con e rendere permanente le chiavi crittografiche e sono di livello superiore e più semplice da usare rispetto a TBS per questi scenari di destinazione.

 

## <a name="developer-audience"></a>Sviluppatori

TBS è progettato per l'uso da parte di sviluppatori di applicazioni basate sui sistemi operativi Windows. Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione Microsoft Windows.

## <a name="run-time-requirements"></a>Requisiti di runtime

La funzionalità TBS richiede almeno Windows Server 2008 o sistema operativo Windows Vista. Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [Informazioni su TBS](about-tbs.md)<br/>         | Concetti chiave e una visualizzazione di alto livello della funzionalità TBS.<br/>               |
| [Uso di TBS](using-tbs.md)<br/>         | Processi e procedure di TBS per l'uso dell'API TBS.<br/>                  |
| [Riferimento a TBS](tbs-reference.md)<br/> | Documentazione sulle funzioni, le strutture e i codici restituiti di TBS.<br/> |



 

 

