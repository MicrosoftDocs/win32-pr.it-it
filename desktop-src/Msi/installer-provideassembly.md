---
description: Il metodo ProvideAssembly dell'oggetto Installer restituisce il percorso installato di un assembly.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Metodo Installer::P rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 45d5c2d6b64936b034d859caddf72ddaaf6fba77451d066205d7f394200311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105211"
---
# <a name="installerprovideassembly-method"></a>Metodo Installer::P rovideAssembly

Il **metodo ProvideAssembly** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso installato di un assembly.

## <a name="syntax"></a>Sintassi


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Assemblea* 
</dt> <dd>

Nome sicuro dell'assembly installato su cui eseguire query.

</dd> <dt>

*appContext* 
</dt> <dd>

Impostare su null per gli assembly globali. Per gli assembly privati, impostare *appContext* sul percorso completo del file di configurazione dell'applicazione o sul percorso completo del file eseguibile dell'applicazione in cui l'assembly è stato reso privato.

</dd> <dt>

*installMode* 
</dt> <dd>

Definisce la modalità di installazione. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                                                              | Significato                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                                | Fornire il componente ed eseguire qualsiasi installazione necessaria per fornire il componente. <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                                           | Specificare il componente solo se la funzionalità esiste. Questa opzione verifica l'esistenza dell'assembly.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                               | Specificare il componente solo se la funzionalità esiste. Questa opzione non verifica l'esistenza dell'assembly.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                                   | Fornisce l'assembly solo se l'assembly è installato in locale.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Combinazione dei flag usati da [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt> </dl> | Chiama il [**metodo ReinstallFeature**](installer-reinstallfeature.md) per reinstallare la funzionalità usando questo parametro per *ReinstallMode* e quindi restituisce il percorso dell'assembly.<br/> |



 

</dd> <dt>

*Assemblyinfo* 
</dt> <dd>

Informazioni sull'assembly e tipo di assembly. Impostare su uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                       | Significato                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiProvideAssemblyNet**</dt> <dt>0</dt> </dl>         | Assembly .NET.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Assembly side-by-side Win32.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Percorso dell'assembly installato.

## <a name="remarks"></a>Commenti

Il **metodo ProvideAssembly** usa la [**funzione MsiProvideAssembly.**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)

## <a name="examples"></a>Esempio

Lo script di esempio seguente illustra l'uso del metodo ProvideAssembly.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




