---
title: Tipo di privacy (Wininet.h)
description: Specifica che le impostazioni di privacy sono relative ai cookie di terze parti o di terze parti.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6f29461f57a2209fde00b30bce7914c207958f27e28062e2c3bd3d94d442e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743728"
---
# <a name="privacy-type"></a>Tipo di privacy

Specifica che le impostazioni di privacy sono relative ai cookie di terze parti o di terze parti.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY \_ TYPE \_ FIRST \_ PARTY**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Si riferisce alle impostazioni di privacy per i cookie di terze parti.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY \_ TYPE \_ THIRD \_ PARTY**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Si riferisce alle impostazioni di privacy per i cookie di terze parti.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I cookie sono classificati come di terze parti e di terze parti. Un cookie di terze parti ha origine dal dominio host. Se " https://www.blueyonderairlines.com " viene trovato nella barra degli indirizzi di Microsoft Internet Explorer, "www.blueyonderairlines.com" è il dominio host. Durante la visita di questa pagina, se un cookie viene impostato da un dominio diverso da "www.blueyonderairlines.com", ad esempio "www.fourthcoffee.com", questo cookie viene considerato un cookie di terze parti.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

