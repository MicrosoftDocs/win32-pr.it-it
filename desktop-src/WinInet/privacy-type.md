---
title: Tipo di privacy (WinInet. h)
description: Specifica che le impostazioni di privacy sono per cookie di terze parti o di terze parti.
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
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874602"
---
# <a name="privacy-type"></a>Tipo di privacy

Specifica che le impostazioni di privacy sono per cookie di terze parti o di terze parti.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**tipo di PRIVACY \_ \_ prima \_ parte**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Fa riferimento alle impostazioni di privacy per i cookie di terze parti.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**tipo di PRIVACY di \_ \_ terze \_ parti**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Fa riferimento alle impostazioni di privacy per i cookie di terze parti.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I cookie sono suddivisi in categorie come la prima e la terza parte. Un cookie di prima entità è quello che ha origine dal dominio host. Se " https://www.blueyonderairlines.com " si trova nella barra degli indirizzi di Microsoft Internet Explorer, "www.blueyonderairlines.com" è il dominio host. Quando si visita questa pagina, se un cookie viene impostato da un dominio diverso da "www.blueyonderairlines.com", ad esempio "www.fourthcoffee.com", il cookie viene considerato un cookie di terze parti.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

