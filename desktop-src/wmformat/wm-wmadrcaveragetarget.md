---
title: WM/WMADRCAverageTarget
description: L'attributo WM/WMADRCAverageTarget contiene il livello di volume medio richiesto dall'utente. Questo valore viene utilizzato da Windows Media Player per il controllo dinamico degli intervalli.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato di Windows Media WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299205"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

L'attributo **WM/WMADRCAverageTarget** contiene il livello di volume medio richiesto dall'utente. Questo valore viene utilizzato da Windows Media Player per il controllo dinamico degli intervalli.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMADRCAverageTarget

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Sono disponibili quattro attributi usati da Windows Media Player per il controllo dinamico degli intervalli: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**. Tutti questi valori vengono impostati dal writer in base alle informazioni provenienti dal codec durante la scrittura di flussi con il codec Windows Media Audio 9 o il codec Windows Media Audio 9 Professional. I valori medi sono impostati sul livello medio del volume del flusso e i valori di picco sono impostati sul livello di volume massimo nel flusso. I valori di riferimento sono di sola lettura. I valori di destinazione vengono impostati da Windows Media Player quando viene riprodotto il file per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.

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

 

 




