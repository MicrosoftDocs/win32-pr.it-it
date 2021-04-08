---
title: Costanti WINBIO_SETTING_SOURCE (tipi WinBio \_ . h)
description: Determinare se la Windows Biometric Framework è attualmente abilitata.
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
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964908"
---
# <a name="winbio_setting_source-constants"></a>Costanti di origine dell' \_ impostazione WINBIO \_

Le costanti seguenti vengono usate dalla funzione [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) per determinare se la Windows Biometric Framework è attualmente abilitata. Le costanti specificano la posizione in cui ha avuto origine l'impostazione.



| Costante                                                                                                                                                                                                        | Descrizione                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**\_origine impostazione \_ WINBIO \_ non valida**</dt> </dl> | Impostazione non valida.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**\_impostazione \_ predefinita di origine dell'impostazione WINBIO \_**</dt> </dl> | L'impostazione è stata originata dai criteri predefiniti.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**\_criteri di \_ origine \_ impostazione WINBIO**</dt> </dl>    | L'impostazione è stata originata nel registro di sistema del computer locale.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**WINBIO \_ impostazione \_ origine \_ locale**</dt> </dl>       | L'impostazione è stata creata da Criteri di gruppo<br/>                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





