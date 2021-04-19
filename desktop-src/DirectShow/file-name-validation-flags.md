---
description: Questi flag specificano il comportamento del localizzatore multimediale.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Flag di convalida del nome file (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327925"
---
# <a name="file-name-validation-flags"></a>Flag di convalida del nome file

\[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

Questi flag specificano il comportamento del localizzatore multimediale.



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ \_Controllo VALIDATEF**</dt> <dt>0x01</dt> </dl>                   | Verificare la validità dei nomi file. È necessario impostare questo flag per convalidare i nomi dei file. In caso contrario, gli altri flag non hanno alcun effetto.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ 0x02 \_ popup VALIDATEF**</dt> <dt></dt> </dl>                   | Se un file non è disponibile, visualizzare una finestra di dialogo Apri file per l'utente finale.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ VALIDATEF \_**</dt> <dt>0x04</dt> </dl>                | Se viene individuato un file mancante, visualizzare brevemente una finestra di messaggio con il nome e il percorso del file. Questo flag è particolarmente utile a scopo di test. la finestra di messaggio non è probabilmente adatta per un prodotto finale.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ VALIDATEF \_ sostituire**</dt> <dt>0x08</dt> </dl>             | Se viene individuato un file mancante, aggiornare il nome dell'oggetto di origine. (Valido solo nel metodo [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Usare sempre un file locale, anche se nella rete è presente una versione del file.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt> </dl>                | Non cercare i file mancanti. Se si imposta il flag di controllo VALIDATEF SFN, i nomi dei file vengono ancora convalidati \_ \_ .<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Ignorare gli oggetti di origine silenziati. (Valido solo nel metodo [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).<br/>                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




