---
title: Stili del controllo SysLink (CommCtrl. h)
description: Le costanti di stile seguenti vengono usate per la creazione di controlli SysLink.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327598"
---
# <a name="syslink-control-styles"></a>Stili del controllo SysLink

Le costanti di stile seguenti vengono usate per la creazione di controlli SysLink.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**\_SecurityTransparent trasparente**</dt> </dl>             | La modalità di combinazione dello sfondo è trasparente. <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>Garanzia di stato **\_ IGNORERETURN**</dt> </dl>       | Quando il collegamento ha lo stato attivo della tastiera e l'utente preme INVIO, la sequenza di tasti viene ignorata dal controllo e passata alla finestra di dialogo host.<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**con \_ prefisso di stato**</dt> </dl>                      | **Windows Vista**. Se il testo contiene una e commerciale, viene considerato come un carattere letterale anziché come prefisso per un tasto di scelta rapida.<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>Garanzia di stato **\_ USEVISUALSTYLE**</dt> </dl> | **Windows Vista**. Il collegamento viene visualizzato nello stile di visualizzazione corrente.<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**USECUSTOMTEXT di garanzia \_**</dt> </dl>       | **Windows Vista**. Quando il controllo viene disegnato, viene inviata una notifica [ \_ CUSTOMTEXT Nm](nm-customtext.md) , in modo che l'applicazione possa fornire il testo in modo dinamico.<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**diritto di garanzia a \_ destra**</dt> </dl>                               | **Windows Vista**. Il testo è giustificato a destra.<br/>                                                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





