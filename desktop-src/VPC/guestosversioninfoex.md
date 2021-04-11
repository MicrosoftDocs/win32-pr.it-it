---
title: Struttura GUESTOSVERSIONINFOEX (VPCCOMInterfaces. h)
description: Contiene informazioni sulla versione del sistema operativo per il sistema operativo guest.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Struttura GUESTOSVERSIONINFOEX Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120170"
---
# <a name="guestosversioninfoex-structure"></a>Struttura GUESTOSVERSIONINFOEX

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contiene informazioni sulla versione del sistema operativo per il sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>Members

<dl> <dt>

**dwOSVersionInfoSize**
</dt> <dd>

Dimensioni in byte della struttura di dati. Impostare questo membro su `sizeof(GUESTOSVERSIONINFOEX)` .

</dd> <dt>

**dwMajorVersion**
</dt> <dd>

Numero di versione principale.

</dd> <dt>

**dwMinorVersion**
</dt> <dd>

Numero di versione secondario.

</dd> <dt>

**dwBuildNumber**
</dt> <dd>

Numero di build.

</dd> <dt>

**dwPlatformId**
</dt> <dd>

Piattaforma del sistema operativo. Questo membro può essere **una \_ piattaforma ver \_ Win32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Stringa con terminazione null, ad esempio "Service Pack 3", che indica il Service Pack più recente installato nel sistema. Se non è stato installato alcun Service Pack, la stringa è vuota.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Il numero di versione principale del Service Pack più recente installato.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

Il numero di versione secondario del Service Pack più recente installato.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Maschera di maschera che identifica i gruppi di prodotti disponibili nel sistema. Questo membro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**Ver \_ SUITE \_ BackOffice**</dt> <dt>0x00000004</dt> </dl>                                            | Microsoft BackOffice Components è installato.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**Ver \_ 0x00000400 \_ Blade Suite**</dt> <dt></dt> </dl>                                                           | Windows Server 2003, Web Edition è installato.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**Ver \_ \_ \_ Server di calcolo Suite**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition è installato.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**Ver \_ SUITE \_ datacenter**</dt> <dt>0x00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server è installato.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server è installato. Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded è installato.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**Ver \_ 0x00000200 \_ personali Suite**</dt> <dt></dt> </dl>                                                  | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Desktop remoto è supportato, ma è supportata una sola sessione interattiva. Questo valore viene impostato a meno che il sistema non sia in esecuzione in modalità server applicazioni.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**Ver \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows. Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**Ver \_ SUITE \_ SMALLBUSINESS con \_ restrizioni**</dt> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore. Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**Ver \_ SUITE \_ storage \_ server**</dt> <dt>0x00002000</dt> </dl>                               | Windows Storage Server 2003 R2 o Windows Storage Server 2003 è installato.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**Ver \_ 0x00000010 \_ terminale Suite**</dt> <dt></dt> </dl>                                                  | Servizi terminal è installato. Questo valore è sempre impostato.<br/> Se è impostato il **\_ \_ terminale ver Suite** , ma **ver \_ Suite \_ SINGLEUSERTS** non è impostato, il sistema viene eseguito in modalità server applicazioni.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**Ver \_ 0x00008000 gruppo di \_ \_ server wh**</dt> <dt></dt> </dl>                                              | Windows Home Server è installato.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Eventuali ulteriori informazioni sul sistema. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**Ver \_ \_ \_ Controller di dominio NT**</dt> <dt>0x0000002</dt> </dl> | Il sistema è un controller di dominio e il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**Ver \_ NT \_ Server**</dt> <dt>0x0000003</dt> </dl>                                   | Il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/> Si noti che un server che è anche un controller di dominio viene segnalato come **\_ controller di \_ dominio \_ ver NT**, non come **\_ \_ Server ver NT**.<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**Ver \_ \_Workstation NT**</dt> <dt>0x0000001</dt> </dl>                    | Il sistema operativo è Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

