---
title: Costanti ed enumerazioni WinRM
description: Gestione remota Windows dispone di flag di bit utilizzati per la creazione di sessioni ed enumerazioni e per i tipi di accesso e l'autenticazione a un server proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045017"
---
# <a name="winrm-constants-and-enumerations"></a>Costanti ed enumerazioni WinRM

Gestione remota Windows dispone di flag di bit utilizzati per la creazione di sessioni ed enumerazioni e per i tipi di accesso e l'autenticazione a un server proxy. Nell'elenco seguente sono elencati i diversi flag di bit.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Costanti di sessione](session-constants.md)
</dt> <dd>

Flag utilizzati nel parametro *Flags* dei metodi [**WSMan. CreateSession**](wsman-createsession.md) o [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) .

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Costanti di enumerazione**](enumeration-constants.md)
</dt> <dd>

Flag utilizzati nel parametro *Flags* della chiamata a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Flag utilizzati nel parametro *authenticationMechanism* della chiamata a [**IWSManConnectionOptionsEx2:: seproxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Flag utilizzati nel parametro *AccessType* della chiamata a [**IWSManConnectionOptionsEx2:: seproxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2:: seproxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




