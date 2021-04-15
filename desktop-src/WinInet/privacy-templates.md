---
title: Modelli di privacy (WinInet. h)
description: Di seguito sono riportati i livelli di privacy che equivalgono alle regole per accettare, accettare in modo condizionale o non accettare cookie.
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
ms.openlocfilehash: e9394068721920836f61871ca42471469fd4c592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479270"
---
# <a name="privacy-templates"></a>Modelli di privacy

Di seguito sono riportati i livelli di privacy che equivalgono alle regole per accettare, accettare in modo condizionale o non accettare cookie. Questi livelli corrispondono ai livelli di preferenza sulla privacy impostati nella scheda privacy in Opzioni Internet. Per le definizioni dettagliate, vedere [privacy in Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) .

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**\_modello privacy \_ senza \_ cookie**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Equivale a **blocca tutti i cookie** sulla barra del dispositivo di scorrimento delle preferenze sulla privacy in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**\_modello privacy \_ alto**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Questa operazione è identica alla barra del dispositivo di scorrimento **Preferenze per la** privacy in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**modello di PRIVACY \_ \_ medio \_ alto**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Equivale a **media \_ High** sulla barra del dispositivo di scorrimento delle preferenze sulla privacy in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**modello di PRIVACY \_ \_ medio**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Equivale a **media** sulla barra del dispositivo di scorrimento delle preferenze sulla privacy in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**modello di PRIVACY \_ \_ medio \_ basso** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



È uguale a **low** sulla barra del dispositivo di scorrimento delle preferenze sulla privacy in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**modello di PRIVACY \_ \_ basso**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Questo equivale a **accettare tutti i cookie** sulla barra del dispositivo di scorrimento delle preferenze per la privacy in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**modello di PRIVACY \_ \_ personalizzato**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Definito dall'utente. Per informazioni su come impostare le impostazioni di privacy personalizzate, vedere [come creare un file di importazione della privacy personalizzato](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) .


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**modello di PRIVACY \_ \_ avanzato**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Definito dall'utente. Le opzioni avanzate sono impostate nella finestra di dialogo **Impostazioni avanzate** per la privacy raggiungibili dalla scheda **privacy** in **Opzioni Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**\_modello privacy \_ Max**
</dt> <dd> <dl> <dt>

modello di PRIVACY \_ \_ basso
</dt> <dt>



Uguale al **modello di privacy \_ \_ basso**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

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

 

