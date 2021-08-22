---
title: WM/WMADRCPeakTarget
description: L'attributo WM/WMADRCPeakTarget contiene il livello massimo di volume richiesto dall'utente. Questo valore viene usato dall'Windows Media Player per il controllo di intervallo dinamico.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- WM/WMADRCPeakTarget windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590681"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

**L'attributo WM/WMADRCPeakTarget** contiene il livello massimo di volume richiesto dall'utente. Questo valore viene usato dall'Windows Media Player per il controllo di intervallo dinamico.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMADRCPeakTarget

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

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




