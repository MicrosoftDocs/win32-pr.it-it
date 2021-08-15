---
title: Metodo FetchReportSummaryEntries della classe Win32_TSLicenseReport
description: Recupera i riepiloghi Servizi Desktop remoto licenze di accesso client per utente (Servizi Desktop remoto \ 160; Cal cal per utente) dal report.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Metodo FetchReportSummaryEntries Servizi Desktop remoto
- Metodo FetchReportSummaryEntries Servizi Desktop remoto , Win32_TSLicenseReport classe
- Win32_TSLicenseReport classe Servizi Desktop remoto , metodo FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094d7fe1f7aa3d5acabce7d7d248c16601b5005d09f2583cc23c7390c3642361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348576"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportSummaryEntries della classe \_ Win32 TSLicenseReport

Recupera i riepiloghi Servizi Desktop remoto licenze CAL client per utente (CAL Per Utente di Servizi Desktop remoto) dal report.

## <a name="syntax"></a>Sintassi


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartIndex* \[ Pollici\]
</dt> <dd>

Indice della prima voce del report da ricevere. La prima voce del report ha un indice pari a zero.

</dd> <dt>

*Conteggio* \[ in, out\]
</dt> <dd>

Numero di voci del report da recuperare dall'oggetto report. Il valore zero indica che tutte le voci del report a partire da *StartIndex* devono essere recuperate. In caso di restituzione, contiene il numero di voci nella matrice *ReportSummaryEntries.*

</dd> <dt>

*ReportSummaryEntries* \[ Cambio\]
</dt> <dd>

Restituisce una matrice di [**classi \_ Win32 TSLicenseReportSummaryEntry.**](win32-tslicensereportsummaryentry.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Il valore **LSERVER \_ I NO MORE \_ \_ \_ DATA** (0x4001) indica che non sono presenti altre voci del report.

## <a name="remarks"></a>Commenti

Non si tratta di un metodo statico. Questo metodo deve essere chiamato da un oggetto report sull'utilizzo delle licenze per utente.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

