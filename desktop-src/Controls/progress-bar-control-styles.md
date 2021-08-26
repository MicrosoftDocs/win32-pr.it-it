---
title: Stili del controllo Indicatore di stato (CommCtrl.h)
description: I controlli Indicatore di stato supportano gli stili di controllo seguenti
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1216171b116bffb962b3ebfe1a76497473cf2db2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465277"
---
# <a name="progress-bar-control-styles"></a>Stili del controllo Indicatore di stato

I controlli Indicatore di stato supportano gli [stili di controllo](progress-bar-control.md) seguenti:




| Costante | Descrizione | 
|----------|-------------|
| <span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl><dt><strong>PBS_MARQUEE</strong></dt></dl> | <a href="common-control-versions.md">Versione 6.0</a> o successiva. Le dimensioni dell'indicatore di stato non aumentano, ma si spostano ripetutamente lungo la lunghezza della barra, indicando l'attività senza specificare la proporzione dello stato di avanzamento completata. <br /><blockquote>[!Note]<br />Comctl32.dll versione 6 non è ridistribuibile, ma è incluso in Windows o versioni successive. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione.</a></blockquote><br /> | 
| <span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl><dt><strong>PBS_SMOOTH</strong></dt></dl> | <a href="common-control-versions.md">Versione 4.70</a> o successiva. L'indicatore di stato visualizza lo stato di avanzamento in una barra di scorrimento uniforme anziché nella barra segmentata predefinita. <br /><blockquote>[!Note]<br />Questo stile è supportato solo nel tema Windows classico. Tutti gli altri temi eseguono l'override di questo stile.</blockquote><br /> | 
| <span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl><dt><strong>PBS_SMOOTHREVERSE</strong></dt></dl> | <a href="common-control-versions.md">Versione 6.0 o</a> successiva e Windows <strong>Vista.</strong> Determina il comportamento dell'animazione che l'indicatore di stato deve usare quando si sposta indietro (da un valore superiore a un valore inferiore). Se questa proprietà è impostata, si verificherà una transizione "uniforme". In caso contrario, il controllo "passa" al valore inferiore.<br /> | 
| <span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl><dt><strong>PBS_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Versione 4.70</a> o successiva. L'indicatore di stato visualizza lo stato di avanzamento verticalmente, dal basso verso l'alto.<br /> | 




## <a name="remarks"></a>Commenti

È possibile impostare gli stili dell'indicatore di stato, come per altri controlli comuni, con [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)o [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

