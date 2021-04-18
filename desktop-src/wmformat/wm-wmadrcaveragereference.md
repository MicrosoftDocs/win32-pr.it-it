---
title: WM/WMADRCAverageReference
description: L'attributo WM/WMADRCAverageReference contiene il livello di volume medio del file come codificato.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Formato di Windows Media WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299207"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

L'attributo **WM/WMADRCAverageReference** contiene il livello di volume medio del file come codificato.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMADRCAverageReference

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Sono disponibili quattro attributi usati da Windows Media Player per il controllo dinamico degli intervalli: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**. Tutti questi valori vengono impostati dal writer in base alle informazioni provenienti dal codec durante la scrittura di flussi con il codec Windows Media Audio 9 o il codec Windows Media Audio 9 Professional. I valori medi sono impostati sul livello medio del volume del flusso e i valori di picco sono impostati sul livello di volume massimo nel flusso. I valori di riferimento sono di sola lettura. I valori di destinazione vengono impostati da Windows Media Player quando viene riprodotto il file per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.

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

 

 




