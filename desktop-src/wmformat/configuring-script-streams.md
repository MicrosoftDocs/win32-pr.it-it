---
title: Configurazione degli script Flussi
description: Configurazione degli script Flussi
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flussi, configurazione di flussi di script
- codec, configurazione di flussi di script
- flussi di script, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95c4c43fcb29ec2f77dacbf5a66b1c8c36c666d80fd5f5c09779a4ecaf22f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655989"
---
# <a name="configuring-script-streams"></a>Configurazione degli script Flussi

Come tutti i tipi di flusso arbitrari, i flussi di script devono avere una velocità in bit e una finestra del buffer definite per questi tipi. Il tipo di supporto principale nella [**struttura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) deve essere impostato su WMMEDIATYPE \_ Script.

I flussi di script devono avere il membro **formattype** di **WM MEDIA \_ \_ TYPE** impostato su WMFORMAT Script, che indica che il membro \_ **pbFormat** punta a una [**struttura WMSCRIPTFORMAT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)

Esiste un solo tipo di script supportato, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Comandi script**](script-commands.md)
</dt> </dl>

 

 




