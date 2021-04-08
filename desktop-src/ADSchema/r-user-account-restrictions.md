---
title: Set di proprietà dell'account utente-restrizioni
description: Set di proprietà contenente gli attributi utente che descrivono le restrizioni dell'account.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Proprietà dell'account utente-restrizioni impostare AD schema
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3c39c80c83f321c654e675ccd87950cfd4bcf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965061"
---
# <a name="user-account-restrictions-property-set"></a>Set di proprietà dell'account utente-restrizioni

Set di proprietà contenente gli attributi utente che descrivono le restrizioni dell'account.



| Voce | Valore |
|--------------|--------------------------------------|
| CN           | Limitazioni dell'account utente            |
| Display-Name | Limitazioni dell'account                 |
| Rights-GUID  | 4c164200-20c0-11d0-a768-00aa006e0529 |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/>                                                                                                                                                   |
| Localization-display-ID | 9                                                                                                                                                                                                                             |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> [**Controllo account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localization-display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> [**Controllo account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Localization-display-ID | 9                                                                                                                                                                                                     |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localization-display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> [**Controllo account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Localization-display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-user-password-expired-time-calcolato**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> [**Controllo account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localization-display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-user-password-expired-time-calcolato**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> [**Controllo account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localization-display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membri del set di proprietà    | [**Account-scadenza**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-calcolato**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-user-password-expired-time-calcolato**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-ultimo set**](a-pwdlastset.md)<br/> [**Controllo account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



 

 





