---
description: Rappresenta il controllo di registrazione della smart card.
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: Interfaccia ISCrdEnr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 3c3c882020db8b25c587a8d95824b3c90232bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319356"
---
# <a name="iscrdenr-interface"></a>Interfaccia ISCrdEnr

L'interfaccia **ISCrdEnr** rappresenta il controllo di registrazione delle smart card. È principalmente di interesse per gli sviluppatori che non utilizzano l'automazione. Per la programmazione in Visual Basic o in un altro linguaggio di automazione, vedere l'oggetto [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) .

## <a name="members"></a>Membri

L'interfaccia **ISCrdEnr** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCrdEnr** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **ISCrdEnr** dispone di questi metodi.



| Metodo                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**iscriversi**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Richiede un certificato per conto dell'utente e archivia il [*certificato*](../secgloss/c-gly.md) risultante nella [*Smart Card*](../secgloss/s-gly.md)dell'utente.<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Enumera i nomi delle autorità di [*certificazione*](../secgloss/c-gly.md) (CAS) per un determinato nome del modello di certificato.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Enumera i nomi dei modelli di certificato.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Enumera il nome dei [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) disponibili.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Restituisce il numero di CA disponibili per emettere un certificato in base al modello di certificato specificato.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Recupera il nome dell'autorità di certificazione specificata per un modello di certificato specificato.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Recupera il numero di modelli di certificato.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Recupera il nome del modello di certificato.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Determinare se un modello di certificato contiene l' \_ \_ utilizzo della \_ chiave di protezione della posta elettronica szOID PKIX KP \_ . Se questo utilizzo della chiave fa parte del modello di certificato, il modello di certificato supporta le operazioni [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Recupera il nome del certificato risultante da una chiamata precedente riuscita a [**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)). Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Recupera il nome dell'oggetto dal certificato di firma. Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | Cancella il nome utente dal controllo smart card.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Consente di visualizzare una finestra di dialogo **Seleziona certificato** in cui è possibile selezionare un certificato di firma (noto anche come *certificato agente di registrazione*).<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Visualizza una finestra di dialogo **Seleziona utente** che consente di selezionare un nome utente. Il nome utente viene applicato all'utente per conto del quale è destinata la registrazione del certificato.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Specifica il nome dell'autorità di certificazione.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Specifica il nome del modello di certificato.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Specifica un certificato di firma (noto anche come *certificato dell'agente di registrazione*).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Specifica il nome dell'utente per conto del quale è prevista la registrazione del certificato.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Proprietà

L'interfaccia **ISCrdEnr** ha queste proprietà.



| Proprietà                                         | Tipo di accesso           | Descrizione                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Sola lettura<br/>  | Specifica il numero di CSP. Questa proprietà è di sola lettura.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Lettura/Scrittura<br/> | Nome del CSP. Si tratta di una proprietà di lettura/scrittura. <br/>        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



 

 
