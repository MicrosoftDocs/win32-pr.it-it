---
title: Funzioni IPsec
description: Funzioni IPsec
ms.assetid: db656c58-7776-44c4-a7ce-c38e59b37c74
keywords:
- Funzioni IPsec dell'API della piattaforma filtro Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261e767888b4581587ee550bf240c929f6db4531
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299807"
---
# <a name="ipsec-functions"></a>Funzioni IPsec

Di seguito sono riportate le funzioni di Windows Filtering Platform (WFP) che interagiscono con Internet Protocol Security (IPsec).

-   FwpmIPsecTunnelAdd:
    -   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)
    -   [**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)
    -   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)
-   [**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)
-   [**CHECK0 chiave di \_ Gestione chiavi IPSec \_ \_ \_ \_**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**Il \_ gestore delle chiavi IPSec \_ \_ impone \_ Key0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**\_ \_ \_ Notifica Key0 di gestione chiavi IPSec \_**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**\_ \_ CALLBACK0 contesto SA \_ IPSec**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecDospGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetsecurityinfo0)
-   [**IPsecDospGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetstatistics0)
-   [**IPsecDospSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospsetsecurityinfo0)
-   [**IPsecDospStateCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0)
-   [**IPsecDospStateDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatedestroyenumhandle0)
-   [**IPsecDospStateEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstateenum0)
-   IPsecGetStatistics:
    -   [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)
    -   [**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 e versioni successive)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   IPsecSaContextAddInbound:
    -   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)
    -   [**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 e versioni successive)
-   IPsecSaContextAddOutbound:
    -   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)
    -   [**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 e versioni successive)
-   IPsecSaContextCreate:
    -   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)
    -   [**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 e versioni successive)
-   [**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)
-   [**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)
-   [**IPsecSaContextDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0)
-   IPsecSaContextEnum:
    -   [**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)
    -   [**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 e versioni successive)
-   [**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)
-   IPsecSaContextGetById:
    -   [**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)
    -   [**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 e versioni successive)
-   IPsecSaContextGetSpi:
    -   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)
    -   [**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 e versioni successive)
-   [**IPsecSaContextSetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsetspi0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUpdate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [**IPsecSaContextUpdate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)
-   [**IPsecSaDbGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0)
-   [**IPsecSaDbSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbsetsecurityinfo0)
-   [**IPsecSaDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0)
-   IPsecSaEnum:
    -   [**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)
    -   [**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 e versioni successive)

 

 