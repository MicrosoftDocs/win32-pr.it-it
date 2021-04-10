---
title: Messaggio di EM_DISPLAYBAND (RichEdit. h)
description: Visualizza una parte del contenuto di un controllo Rich Edit, come in precedenza formattato per un dispositivo usando il \_ messaggio FormatRange em.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Controlli di Windows Message EM_DISPLAYBAND
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
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964479"
---
# <a name="em_displayband-message"></a>\_Messaggio DISPLAYBAND em

Visualizza una parte del contenuto di un controllo Rich Edit, come in precedenza formattato per un dispositivo usando il messaggio [**\_ FormatRange em**](em-formatrange.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica l'area di visualizzazione del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è **true**.

Se l'operazione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Gli oggetti Text e Component Object Model (COM) vengono ritagliati dal rettangolo. Non è necessario che l'applicazione imposti l'area di visualizzazione.

La banda è il processo mediante il quale viene generata una singola pagina di output utilizzando uno o più rettangoli o bande separate. Quando tutte le bande vengono posizionate nella pagina, viene generato un risultato di un'immagine completa. Questo approccio viene spesso usato dalle stampanti raster che non dispongono di memoria sufficiente o della possibilità di creare un'immagine di una pagina intera in una sola volta. I dispositivi di banda includono la maggior parte delle stampanti a matrice punto, oltre ad alcune stampanti laser.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa di controlli Rich Edit](printing-rich-edit-controls.md)
</dt> </dl>

 

