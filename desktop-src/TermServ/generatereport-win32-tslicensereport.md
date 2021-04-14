---
title: Metodo GenerateReport della classe Win32_TSLicenseReport (gpmgmt. h)
description: GenerateReport non è più disponibile per l'uso a partire da Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GenerateReport
- Metodo GenerateReport Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400791"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Metodo GenerateReport della \_ classe TSLicenseReport Win32

\[**GenerateReport** non è più disponibile per l'uso a partire da Windows Server 2012. Usare invece [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]

Questo metodo non è supportato.

**Windows server 2008 R2 e Windows server 2008:** Genera un report di utilizzo delle licenze per utente corrente nel server licenze Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ScopeType* \[ in\]
</dt> <dd>

Ambito del report utilizzo licenze. Può contenere i valori seguenti.

<dt>

1
</dt> <dd>

Il report verrà generato per l'intero dominio.

</dd> <dt>

2
</dt> <dd>

Il report verrà generato per l'unità organizzativa (OU) specificata nel parametro *ScopeValue* .

</dd> <dt>

3
</dt> <dd>

Il report verrà generato per tutti i domini trusted.

</dd> </dl> </dd> <dt>

*ScopeValue* \[ in\]
</dt> <dd>

Se il parametro *ScopeType* è 2, *ScopeType* specifica l'unità organizzativa per la quale verrà generato il report. È necessario specificare *ScopeValue* usando il formato **ou =**_OUName1_*_, ou =_*_OUName2_*_..._*.

</dd> <dt>

*Nome file* \[ out\]
</dt> <dd>

Nome file del report generato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **WBEM \_ E \_ non \_ supportato**.

**Windows server 2008 R2 e Windows server 2008:** Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Si tratta di un metodo statico.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                                 |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                         |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>Gpmgmt. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> </dl>

 

