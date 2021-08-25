---
title: Set di proprietà User-Account-Restrictions
description: Set di proprietà contenente gli attributi utente che descrivono le restrizioni dell'account.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Set di proprietà User-Account-Restrictions schema di AD
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050fe70f98bb0bb6fbb457e0540fa61bce9c8f61c2769cf24fb09aa87189d022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702721"
---
# <a name="user-account-restrictions-property-set"></a>Set di proprietà User-Account-Restrictions

Set di proprietà contenente gli attributi utente che descrivono le restrizioni dell'account.



| Voce | Valore |
|--------------|--------------------------------------|
| CN           | Restrizioni dell'account utente            |
| Display-Name | Restrizioni dell'account                 |
| Rights-GUID  | 4c164200-20c0-11d0-a768-00aa006e0529 |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/>                                                                                                                                                   |
| Localization-Display-ID | 9                                                                                                                                                                                                                             |
| Membri del set di proprietà    | [**Scadenza dell'account**](a-accountexpires.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Controllo dell'account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localization-Display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membri del set di proprietà    | [**Scadenza dell'account**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Controllo dell'account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Localization-Display-ID | 9                                                                                                                                                                                                     |
| Membri del set di proprietà    | [**Scadenza dell'account**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localization-Display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membri del set di proprietà    | [**Scadenza dell'account**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Controllo dell'account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Localization-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membri del set di proprietà    | [**Scadenza dell'account**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Controllo dell'account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localization-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membri del set di proprietà    | [**Scadenza account**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd- Ultimo set**](a-pwdlastset.md)<br/> [**Controllo dell'account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utente**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localization-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membri del set di proprietà    | [**Scadenza account**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd- Ultimo set**](a-pwdlastset.md)<br/> [**Controllo dell'account utente**](a-useraccountcontrol.md)<br/> [**Parametri utente**](a-userparameters.md)<br/> |



 

 





