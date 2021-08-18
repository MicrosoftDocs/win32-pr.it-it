---
title: Metodo FetchReportEntries della classe Win32_TSLicenseReport
description: Recupera i dettagli delle licenze Servizi Desktop remoto di accesso client per utente (Servizi Desktop remoto \ 160; Cal cal per utente) dal report. Ogni voce rappresenta un'istanza di Servizi Desktop remoto \ 160; Licenza CAL per utente attualmente in uso.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Metodo FetchReportEntries Servizi Desktop remoto
- Metodo FetchReportEntries Servizi Desktop remoto , Win32_TSLicenseReport classe
- Win32_TSLicenseReport classe Servizi Desktop remoto , metodo FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35c2af0578b0b130b5ef92bae5d374cc4ba2ba82c172689d00782e68b65c143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871731"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportEntries della classe \_ TSLicenseReport Win32

Recupera i dettagli delle licenze Servizi Desktop remoto per utente (LICENZE CAL Per Utente di Servizi Desktop remoto) dal report. Ogni voce rappresenta una licenza CAL Per Utente di Servizi Desktop remoto attualmente in uso.

## <a name="syntax"></a>Sintassi


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
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

Numero di voci del report da recuperare dall'oggetto report. Il valore zero indica che tutte le voci del report a partire da *StartIndex* devono essere recuperate. In caso di restituzione, contiene il numero di voci nella matrice *ReportEntries.*

</dd> <dt>

*ReportEntries* \[ Cambio\]
</dt> <dd>

Restituisce una matrice di [**classi \_ TSLicenseReportEntry Win32.**](win32-tslicensereportentry.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Il valore **LSERVER \_ I NO MORE \_ \_ \_ DATA** (0x4001) indica che non sono presenti altre voci del report.

## <a name="remarks"></a>Commenti

Non si tratta di un metodo statico. Questo metodo deve essere chiamato da un oggetto report sull'utilizzo delle licenze per utente.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

