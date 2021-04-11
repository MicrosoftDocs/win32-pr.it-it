---
title: Configurazione di flussi di script
description: Configurazione di flussi di script
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flussi, configurazione di flussi di script
- codec, configurazione di flussi di script
- flussi di script, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044587"
---
# <a name="configuring-script-streams"></a>Configurazione di flussi di script

Come tutti i tipi di flusso arbitrari, i flussi di script devono avere una velocità in bit e una finestra del buffer definiti. Il tipo di supporto principale nella struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) deve essere impostato su WMMEDIATYPE \_ script.

Per i flussi di script è necessario che il membro **formatType** del **\_ \_ tipo di supporto WM** sia impostato su WMFORMAT \_ script, che indica che il membro **pbFormat** punta a una struttura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .

È disponibile un solo tipo di script supportato, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Comandi script**](script-commands.md)
</dt> </dl>

 

 




