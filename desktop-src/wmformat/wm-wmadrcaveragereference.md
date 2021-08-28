---
title: WM/WMADRCAverageReference
description: L'attributo WM/WMADRCAverageReference contiene il livello di volume medio del file come codificato.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- WM/WMADRCAverageReference windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026949"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

**L'attributo WM/WMADRCAverageReference** contiene il livello di volume medio del file come codificato.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMADRCAverageReference

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Esistono quattro attributi usati da Windows Media Player per il controllo di intervallo dinamico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**. Tutti questi valori vengono impostati dal writer in base alle informazioni del codec durante la scrittura di flussi con il codec Windows Media Audio 9 o Windows Media Audio 9 Professional codec. I valori medi vengono impostati sul livello di volume medio del flusso e i valori di picco vengono impostati sul livello massimo del volume nel flusso. I valori di riferimento sono di sola lettura. I valori di destinazione vengono impostati Windows Media Player quando il file viene riprodotto per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




