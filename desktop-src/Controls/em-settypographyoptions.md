---
title: Messaggio di EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Imposta lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Controlli di Windows Message EM_SETTYPOGRAPHYOPTIONS
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964385"
---
# <a name="em_settypographyoptions-message"></a>\_Messaggio SETTYPOGRAPHYOPTIONS em

Imposta lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o entrambi i valori seguenti.



| Valore                                                                                                                                                                                    | Significato                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**A \_ ADVANCEDTYPOGRAPHY**</dt> </dl> | L'interruzioni di riga e la formattazione di riga avanzate sono attivate. <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**a \_ SIMPLELINEBREAK**</dt> </dl>             | Interruzioni di riga più veloci per testo semplice (richiede **\_ ADVANCEDTYPOGRAPHY**). <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera costituita da uno o più flag in *wParam*. Verranno impostati o cancellati solo i flag impostati in questa maschera. In questo modo è possibile impostare o cancellare un flag singolo senza leggere gli Stati del flag corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se *wParam* è valido; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

L'interruzioni di riga avanzate viene attivata automaticamente dal controllo Rich Edit quando necessario, ad esempio per la gestione di alfabeti non latini, come l'arabo e l'ebraico, e per la matematica. È necessario anche per i paragrafi giustificati, la sillabazione e altre funzionalità tipografiche.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETTYPOGRAPHYOPTIONS em**](em-gettypographyoptions.md)
</dt> </dl>

 

 





