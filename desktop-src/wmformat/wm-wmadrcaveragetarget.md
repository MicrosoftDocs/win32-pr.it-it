---
title: WM/WMADRCAverageTarget
description: L'attributo WM/WMADRCAverageTarget contiene il livello medio di volume richiesto dall'utente. Questo valore viene usato dall'Windows Media Player per il controllo di intervallo dinamico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- WM/WMADRCAverageTarget windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd08dd09b6db671a0af1d816162923624cb781148f557ce4bee21fe2dc9a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083915"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

**L'attributo WM/WMADRCAverageTarget** contiene il livello medio di volume richiesto dall'utente. Questo valore viene usato dall'Windows Media Player per il controllo di intervallo dinamico.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMADRCAverageTarget

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Esistono quattro attributi usati da Windows Media Player per il controllo di intervallo dinamico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**. Tutti questi valori vengono impostati dal writer in base alle informazioni del codec durante la scrittura di flussi con il codec Windows Media Audio 9 o Windows Media Audio 9 Professional codec. I valori medi vengono impostati sul livello di volume medio del flusso e i valori di picco vengono impostati sul livello massimo del volume nel flusso. I valori di riferimento sono di sola lettura. I valori di destinazione vengono impostati Windows Media Player quando il file viene riprodotto per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




