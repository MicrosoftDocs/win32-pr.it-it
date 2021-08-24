---
title: EM_DISPLAYBAND messaggio (Richedit.h)
description: Visualizza una parte del contenuto di un controllo Rich Edit, come formattato in precedenza per un dispositivo usando il messaggio \_ EM FORMATRANGE.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67fc951940d76dced2851a01b7049b053f3e3c2b45f6eee95eb27bef633f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915941"
---
# <a name="em_displayband-message"></a>Messaggio \_ EM DISPLAYBAND

Visualizza una parte del contenuto di un controllo Rich Edit, come formattato in precedenza per un dispositivo usando il [**messaggio \_ EM FORMATRANGE.**](em-formatrange.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) che specifica l'area di visualizzazione del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è **TRUE.**

Se l'operazione non riesce, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Il testo e Component Object Model oggetti (COM) vengono ritagliati dal rettangolo. L'applicazione non deve impostare l'area di ritaglio.

Banding è il processo tramite il quale viene generata una singola pagina di output usando uno o più rettangoli separati o bande. Quando tutte le bande vengono posizionate nella pagina, viene restituita un'immagine completa. Questo approccio viene spesso usato dalle stampanti raster che non hanno memoria sufficiente o non sono in grado di creare un'immagine di una pagina intera contemporaneamente. I dispositivi a banda includono la maggior parte delle stampanti a matrice di punti, nonché alcune stampanti a colori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa di controlli Rich Edit](printing-rich-edit-controls.md)
</dt> </dl>

 

