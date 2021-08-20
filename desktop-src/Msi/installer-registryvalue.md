---
description: Il metodo RegistryValue dell'oggetto Installer legge le informazioni su una chiave del Registro di sistema specificata.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Metodo Installer.RegistryValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: eea77074a19ada084493bf5e24edaf49e25b659b0accdad16dab6c5781078f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074921"
---
# <a name="installerregistryvalue-method"></a>Metodo Installer.RegistryValue

Il **metodo RegistryValue** dell'oggetto [**Installer**](installer-object.md) legge le informazioni su una chiave del Registro di sistema specificata. Se la chiave o il valore specificato non esiste, il metodo restituisce un errore di 9, "Indice non compreso nell'intervallo".

## <a name="syntax"></a>Sintassi


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*radice* 
</dt> <dd>

In Windows NT 4.0, la radice del Registro di sistema è una chiave radice numerica o un nome di computer come stringa. I nomi dei computer sono sempre stringhe. In Windows 95, Windows 98 o Windows Me, la radice del Registro di sistema è solo una chiave radice numerica. È possibile accedere a HKLM solo in un computer remoto.



| Radice                                                                                                                                                                                   | Significato      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**HKEY \_ CLASSES \_ ROOT**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**HKEY \_ CURRENT \_ USER**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**HKEY \_ LOCAL \_ MACHINE**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**UTENTI \_ HKEY**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**DATI SULLE PRESTAZIONI \_ DI \_ HKEY**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**HKEY \_ CURRENT \_ CONFIG**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**HKEY \_ DYN \_ DATA**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

Stringa contenente il percorso completo della chiave dalla radice.

</dd> <dt>

*value* 
</dt> <dd>

Questo parametro facoltativo definisce il valore associato da restituire per la chiave specificata. Il valore è uno dei valori illustrati nella tabella seguente.



| Valore                                                                                                                                                                                                    | Significato                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Mancante o vuoto**</dt> </dl> | Restituisce un valore booleano che indica se la chiave esiste.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**Stringa**</dt> </dl>                                         | Restituisce i dati associati al valore denominato, ha esito negativo se il nome del valore non è esistente.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Intero positivo**</dt> </dl> | Restituisce il nome del valore enumerato in base 1, vuoto se inesistente. Questa opzione usa la [**funzione RegEnumValue.**](/windows/win32/api/winreg/nf-winreg-regenumvaluea)<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Numero intero negativo**</dt> </dl> | Restituisce il nome della sottochiave enumerata in base 1, vuoto se inesistente. Questa opzione usa la [**funzione RegEnumKey.**](/windows/win32/api/winreg/nf-winreg-regenumkeya)<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Numero intero zero**</dt> </dl>                 | Restituisce il nome della classe stringa per la chiave designata.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Stringa vuota " "**</dt> </dl> | Restituisce il valore predefinito della chiave del Registro di sistema.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
