---
title: Modelli di privacy (Wininet.h)
description: Di seguito sono riportati i livelli di privacy che equi equitono alle regole per l'accettazione, l'accettazione condizionale o la non accettazione dei cookie.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481aa3e9b6b5b5519bac6e458de1acba90f2cfa20dd0a5babac016d0003c70b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955561"
---
# <a name="privacy-templates"></a>Modelli di privacy

Di seguito sono riportati i livelli di privacy che equi equitono alle regole per l'accettazione, l'accettazione condizionale o la non accettazione dei cookie. Questi livelli corrispondono ai livelli di preferenza di privacy impostati nella scheda Privacy in Opzioni Internet. Vedere [Privacy in Internet Explorer 6 per](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) definizioni dettagliate.

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**MODELLO \_ DI PRIVACY SENZA \_ \_ COOKIE**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Corrisponde a Blocca tutti i **cookie sulla** barra del dispositivo di scorrimento Preferenze privacy in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**PRIVACY \_ TEMPLATE \_ HIGH**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Corrisponde a Alta sulla **barra del** dispositivo di scorrimento Preferenze privacy in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**MODELLO \_ DI PRIVACY \_ \_ MEDIO-ALTO**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Corrisponde a Medio alto sulla **barra \_** del dispositivo di scorrimento Preferenze privacy in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**MODELLO \_ DI PRIVACY \_ MEDIUM**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Corrisponde a Medio sulla **barra del** dispositivo di scorrimento Preferenze privacy in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**MODELLO \_ DI PRIVACY MEDIO \_ \_ BASSO** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Corrisponde a Basso sulla **barra del** dispositivo di scorrimento Preferenze privacy in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**MODELLO \_ DI PRIVACY \_ BASSO**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Corrisponde a Accetta tutti i cookie sulla barra **del** dispositivo di scorrimento Preferenze privacy in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**MODELLO \_ DI PRIVACY \_ PERSONALIZZATO**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Definito dall'utente. Per [informazioni su come configurare le impostazioni di privacy personalizzate,](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) vedere How to Create a Customized Privacy Import File (Come creare un file di importazione della privacy personalizzato).


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**MODELLO \_ DI PRIVACY \_ AVANZATO**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Definito dall'utente. Le opzioni avanzate vengono impostate nella **finestra di dialogo** Impostazioni privacy avanzata raggiungibile dalla scheda **Privacy** in **Opzioni Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**PRIVACY \_ TEMPLATE \_ MAX**
</dt> <dd> <dl> <dt>

MODELLO \_ DI PRIVACY \_ BASSO
</dt> <dt>



Uguale a **PRIVACY \_ TEMPLATE \_ LOW**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

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

 

