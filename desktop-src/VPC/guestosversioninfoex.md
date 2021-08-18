---
title: Struttura GUESTOSVERSIONINFOEX (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 848196448c2bd6f021d85f7c13972e81664dd60a0e4a0bbbd2e05ef3455aade7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056909"
---
# <a name="guestosversioninfoex-structure"></a>Struttura GUESTOSVERSIONINFOEX

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Dimensioni della struttura dei dati, in byte. Impostare questo membro su `sizeof(GUESTOSVERSIONINFOEX)` .

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

Piattaforma del sistema operativo. Questo membro può essere **VER \_ PLATFORM \_ WIN32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Stringa con terminazione Null, ad esempio "Service Pack 3", che indica la versione più recente del Service Pack installata nel sistema. Se non è stato installato alcun Service Pack, la stringa è vuota.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Numero di versione principale del Service Pack più recente installato.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

Numero di versione secondaria del Service Pack più recente installato.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Maschera di bit che identifica i gruppi di prodotti disponibili nel sistema. Questo membro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**VER \_ GRUPPO \_ BACKOFFICE**</dt> <dt>0x00000004</dt> </dl>                                            | Vengono installati i componenti Microsoft BackOffice.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**VER \_ PANNELLO \_ SUITE**</dt> <dt>0x00000400</dt> </dl>                                                           | Windows Server 2003, Web Edition è installato.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**VER \_ SERVER \_ \_ DI CALCOLO SUITE**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition è installato.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**VER \_ SUITE \_ DATACENTER**</dt> <dt>0x00000080</dt> </dl>                                            | Windows È installato Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**VER \_ SUITE \_ ENTERPRISE**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, edizione Enterprise o Windows 2000 Advanced Server è installato. Per altre informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**VER \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded è installato.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**VER \_ SUITE \_ PERSONAL**</dt> <dt>0x00000200</dt> </dl>                                                  | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**VER \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Desktop remoto è supportato, ma è supportata una sola sessione interattiva. Questo valore viene impostato a meno che il sistema non sia in esecuzione in modalità server applicazioni.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**VER \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows. Per altre informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**VER \_ GRUPPO \_ SMALLBUSINESS \_ CON**</dt> <dt>RESTRIZIONI 0x00000020</dt> </dl> | Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore. Per altre informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**VER \_ SERVER \_ DI \_ ARCHIVIAZIONE SUITE**</dt> <dt>0x00002000</dt> </dl>                               | Windows Archiviazione Server 2003 R2 o Windows Archiviazione Server 2003is installato.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**VER \_ \_TERMINALE SUITE**</dt> <dt>0x00000010</dt> </dl>                                                  | Servizi terminal è installato. Questo valore è sempre impostato.<br/> Se **VER SUITE TERMINAL \_ \_ è** impostato ma **VER SUITE \_ \_ SINGLEUSERTS** non è impostato, il sistema è in esecuzione in modalità server applicazioni.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**VER \_ SUITE \_ WH \_ SERVER**</dt> <dt>0x00008000</dt> </dl>                                              | Windows Home Server è installato.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Eventuali informazioni aggiuntive sul sistema. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**VER \_ Controller \_ \_ di dominio NT**</dt> <dt>0x0000002</dt> </dl> | Il sistema è un controller di dominio e il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**VER \_ NT \_ SERVER**</dt> <dt>0x0000003</dt> </dl>                                   | Il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/> Si noti che un server che è anche un controller di dominio viene segnalato come **\_ VER NT DOMAIN \_ \_ CONTROLLER**, non **VER NT \_ \_ SERVER**.<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**VER \_ WORKSTATION \_ NT**</dt> <dt>0x0000001</dt> </dl>                    | Il sistema operativo è Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

