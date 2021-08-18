---
description: Identifica il tipo di host del chiamante WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: WLDP_HOST_ID enumerazione (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: fa52bc6259c75d5bb0929cb25610beb2b143515e2874b09bf04c454397a909e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758381"
---
# <a name="wldp_host_id-enumeration"></a>Enumerazione DELL'ID HOST WLDP \_ \_

Identifica il tipo di host del chiamante WLDP.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ ID \_ HOST \_ SCONOSCIUTO** 
</dt> <dd>

Il tipo di host è sconosciuto.

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ HOST \_ ID \_ GLOBAL**
</dt> <dd>

Il tipo di host è criteri globali.

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP \_ HOST \_ ID \_ VBA**
</dt> <dd>

Il tipo di host è VBScript.

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ HOST \_ ID \_ WSH**
</dt> <dd>

Il tipo di host è Windows Host script.

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ POWERSHELL \_ CON ID \_ HOST**
</dt> <dd>

Il tipo di host Windows PowerShell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ HOST \_ ID \_ IE**
</dt> <dd>

Il tipo di host è Internet Explorer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ ID \_ HOST \_ MSI**
</dt> <dd>

Il tipo di host è Microsoft Windows Installer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ NUMERO \_ MASSIMO DI ID \_ HOST** 
</dt> <dd>

Valore massimo dell'enumerazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl> |



 

 




