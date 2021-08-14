---
title: WINBIO_SETTING_SOURCE costanti (Winbio \_ types.h)
description: Determinare se il Windows Biometric Framework è attualmente abilitato.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f02a5edc80d00d098a592626ad4d9f0e1030f9f6eee119bf615375680d11842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909319"
---
# <a name="winbio_setting_source-constants"></a>Costanti WINBIO \_ SETTING \_ SOURCE

Le costanti seguenti vengono usate dalla funzione [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) per determinare se Windows Biometric Framework è attualmente abilitato. Le costanti specificano la posizione di origine dell'impostazione.



| Costante                                                                                                                                                                                                        | Descrizione                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**ORIGINE IMPOSTAZIONE WINBIO \_ \_ NON \_ VALIDA**</dt> </dl> | L'impostazione non è valida.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA \_ \_ DELL'ORIGINE WINBIO \_**</dt> </dl> | L'impostazione ha origine dai criteri predefiniti.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**CRITERI DI ORIGINE \_ DELL'IMPOSTAZIONE WINBIO \_ \_**</dt> </dl>    | L'impostazione ha avuto origine nel Registro di sistema del computer locale.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**IMPOSTAZIONE LOCALE \_ DELL'ORIGINE WINBIO \_ \_**</dt> </dl>       | L'impostazione è stata creata da Criteri di gruppo<br/>                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





