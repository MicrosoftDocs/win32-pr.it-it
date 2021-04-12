---
title: Metodo FetchReportSummaryEntries della classe Win32_TSLicenseReport
description: Recupera i riepiloghi delle licenze di accesso client di Servizi Desktop remoto per utente (RDS \ 160; Licenze CAL per utente) dal report.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportSummaryEntries
- Metodo FetchReportSummaryEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportSummaryEntries
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
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119115"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Metodo FetchReportSummaryEntries della \_ classe TSLicenseReport Win32

Recupera i riepiloghi delle licenze CAL per utente Servizi Desktop remoto per utente dal report.

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

*StartIndex* \[ in\]
</dt> <dd>

Indice della prima voce del report da ricevere. La prima voce del report ha un indice pari a zero.

</dd> <dt>

*Numero* \[ di in uscita\]
</dt> <dd>

Numero di voci del report da recuperare dall'oggetto report. Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* . Nell'output restituito è contenuto il numero di voci nella matrice *ReportSummaryEntries* .

</dd> <dt>

*ReportSummaryEntries* \[ out\]
</dt> <dd>

Restituisce una matrice di [**classi \_ TSLicenseReportSummaryEntry Win32**](win32-tslicensereportsummaryentry.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Il valore **LSERVER non \_ \_ \_ più \_ dati** (0x4001) indica che non sono presenti altre voci del report.

## <a name="remarks"></a>Commenti

Non si tratta di un metodo statico. Questo metodo deve essere chiamato da un oggetto report utilizzo licenze per utente.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportSummaryEntry Win32**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

