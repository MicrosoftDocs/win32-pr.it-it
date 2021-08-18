---
description: Questi flag specificano il comportamento del localizzatore multimediale.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Flag di convalida dei nomi file (Qedit.h)
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
ms.openlocfilehash: 44bbeebc344edf1c6a9c5a5d287bea7cdfe87e96d9af09a65417411d6cd43820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015769"
---
# <a name="file-name-validation-flags"></a>Flag di convalida dei nomi file

\[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

Questi flag specificano il comportamento del localizzatore multimediale.



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ VALIDATEF \_ CHECK**</dt> <dt>0x01</dt> </dl>                   | Controllare la validità dei nomi di file. È necessario impostare questo flag per convalidare i nomi di file. In caso contrario, gli altri flag non hanno alcun effetto.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ FINESTRA \_ POPUP VALIDATEF**</dt> <dt>0x02</dt> </dl>                   | Se non si trova un file, visualizzare una finestra di dialogo Apri file per l'utente finale.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | Se viene individuato un file mancante, visualizzare brevemente una finestra di messaggio con il nome e il percorso del file. Questo flag è particolarmente utile a scopo di test. la finestra di messaggio probabilmente non è adatta per un prodotto al dettaglio.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ CONVALIDAF \_ REPLACE**</dt> <dt>0x08</dt> </dl>             | Se viene individuato un file mancante, aggiornare il nome dell'oggetto di origine. (Valido solo nel [**metodo IAMTimeline::ValidateSourceNames).**](iamtimeline-validatesourcenames.md)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Usare sempre un file locale, anche se nella rete esiste una versione del file.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ VALIDATEF \_ NOFIND**</dt> <dt>0x20</dt> </dl>                | Non cercare i file mancanti. I nomi di file vengono comunque convalidati se si imposta il flag SFN \_ VALIDATEF \_ CHECK.<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Ignorare gli oggetti di origine disattivati. (Valido solo nel [**metodo IAMTimeline::ValidateSourceNames).**](iamtimeline-validatesourcenames.md)<br/>                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




