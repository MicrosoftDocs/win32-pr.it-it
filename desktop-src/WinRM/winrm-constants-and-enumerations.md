---
title: Costanti ed enumerazioni di WinRM
description: Windows Gestione remota include flag di bit usati nella creazione di sessioni ed enumerazioni e per i tipi di accesso e l'autenticazione a un server proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742937"
---
# <a name="winrm-constants-and-enumerations"></a>Costanti ed enumerazioni di WinRM

Windows Gestione remota include flag di bit usati nella creazione di sessioni ed enumerazioni e per i tipi di accesso e l'autenticazione a un server proxy. Nell'elenco seguente sono elencati i diversi flag di bit.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Costanti di sessione](session-constants.md)
</dt> <dd>

Flag usati nel *parametro flags* dei [**metodi WSMan.CreateSession**](wsman-createsession.md) o [**IWSMan::CreateSession.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Costanti di enumerazione**](enumeration-constants.md)
</dt> <dd>

Flag utilizzati nel *parametro flags* della chiamata [**a Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Flag utilizzati nel *parametro authenticationMechanism* della chiamata a [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Flag utilizzati nel *parametro accessType* della chiamata a [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




