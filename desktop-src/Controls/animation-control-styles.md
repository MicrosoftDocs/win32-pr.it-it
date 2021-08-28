---
title: Stili del controllo Animation (CommCtrl.h)
description: Questa sezione elenca gli stili della finestra usati con i controlli di animazione.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aff6116433533bdc79535be0e282cb81baa9368f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470623"
---
# <a name="animation-control-styles"></a>Stili dei controlli di animazione

Questa sezione elenca gli stili della finestra usati con i controlli di animazione.




| Costante | Descrizione | 
|----------|-------------|
| <span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl><dt><strong>ACS_AUTOPLAY</strong></dt></dl> | Avvia la riproduzione dell'animazione non appena viene aperto il clip AVI. <br /> | 
| <span id="ACS_CENTER"></span><span id="acs_center"></span><dl><dt><strong>ACS_CENTER</strong></dt></dl> | Centra l'animazione nella finestra del controllo di animazione. <br /> | 
| <span id="ACS_TIMER"></span><span id="acs_timer"></span><dl><dt><strong>ACS_TIMER</strong></dt></dl> | Per impostazione predefinita, il controllo crea un thread per riprodurre il clip AVI. Se si imposta questo flag, il controllo riproduce il clip senza creare un thread. internamente il controllo usa un timer Win32 per sincronizzare la riproduzione. <br /><strong>Comctl32.dll versione 6 e successive:</strong> Questo stile non è supportato. Per impostazione predefinita, il controllo riproduce il clip AVI senza creare un thread.<br /><blockquote>[!Note]<br />Comctl32.dll versione 6 non è ridistribuibile. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</blockquote><br /> | 
| <span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl><dt><strong>ACS_TRANSPARENT</strong></dt></dl> | Consente di associare il colore di sfondo di un'animazione a quello della finestra sottostante, creando uno sfondo "trasparente". L'elemento padre del controllo di animazione non deve avere lo stile WS_CLIPCHILDREN (vedere <a href="/windows/desktop/winmsg/window-styles">Stili finestra</a>). Il controllo invia un <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> messaggio al relativo elemento padre. Usare <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> per impostare il colore di sfondo per il contesto di dispositivo su un valore appropriato. Il controllo interpreta il pixel superiore sinistro del primo fotogramma come colore di sfondo predefinito dell'animazione. Verrà nuovamente mappato tutti i pixel con quel colore al valore fornito in risposta alla WM_CTLCOLORSTATIC. <br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



