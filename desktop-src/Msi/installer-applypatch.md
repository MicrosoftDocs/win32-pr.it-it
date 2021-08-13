---
description: Per ogni prodotto elencato dal pacchetto patch come idoneo per la ricezione della patch, il metodo ApplyPatch dell'oggetto Installer richiama un'installazione e imposta la proprietà PATCH sul percorso del pacchetto di patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Metodo Installer.ApplyPatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c4bcb1ba1dc988f3c28188b4b448dba611b83c6cffbe7f942710569ac089776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633228"
---
# <a name="installerapplypatch-method"></a>Metodo Installer.ApplyPatch

Per ogni prodotto elencato dal pacchetto patch come idoneo per la ricezione della patch, il metodo **ApplyPatch** dell'oggetto [**Installer**](installer-object.md) richiama un'installazione e imposta la proprietà [**PATCH**](patch.md) sul percorso del pacchetto di patch.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PatchPackage* 
</dt> <dd>

Specifica un percorso del pacchetto di patch.

</dd> <dt>

*InstallPackage* 
</dt> <dd>

Se *InstallType* è impostato su msiInstallTypeNetworkImage, *InstallPackage* specifica il percorso del prodotto a cui applicare le patch. Se *InstallType è* impostato su msiInstallTypeDefault e *InstallPackage* è impostato su 0, il programma di installazione applica la patch a tutti i prodotti idonei elencati nel pacchetto di patch.

Se *InstallType* è msiInstallTypeSingleInstance, il programma di installazione applica la patch al prodotto specificato da *InstallPackage*. In questo caso, gli altri prodotti idonei elencati nel pacchetto di patch vengono ignorati e il *parametro InstallPackage* contiene la stringa con terminazione Null che rappresenta il codice prodotto dell'istanza di cui applicare la patch. Questo tipo di installazione richiede la versione Windows Installer fornita con Windows Server 2003 o versione successiva o Windows Installer XP SP1 o versioni successive.

</dd> <dt>

*InstallType* 
</dt> <dd>

Questo parametro specifica il tipo di installazione a cui applicare patch. Il *parametro InstallType* viene ignorato se *InstallPackage* viene omesso.



| Valore                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Indica un'installazione amministrativa. In questo caso, *InstallPackage* deve essere impostato su un percorso del pacchetto. Il valore 1 per msiInstallTypeNetworkImage specifica un'installazione amministrativa.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Cerca nel sistema i prodotti di cui applicare le patch. In questo caso, *InstallPackage* deve essere una stringa vuota.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Applicare patch al prodotto specificato da *InstallPackage*. *InstallPackage è* il codice prodotto dell'istanza di a cui applicare la patch. Questo tipo di installazione richiede la versione Windows Installer fornita con Windows Server 2003 o versione successiva o Windows Installer XP SP1 o versioni successive. Per altre informazioni, vedere [Installazione di più istanze di prodotti e patch.](installing-multiple-instances-of-products-and-patches.md)<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Specifica le impostazioni delle proprietà da impostare nella riga di comando. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Poiché il delimitatore di elenco per trasformazioni, origini e patch è un punto e virgola, questo carattere non deve essere usato per i nomi di file o i percorsi.

La [**proprietà REINSTALL**](reinstall.md) è obbligatoria quando si applica un aggiornamento di piccole dimensioni [o](small-updates.md) una patch di [aggiornamento secondaria.](minor-upgrades.md) Senza questa proprietà, la patch viene registrata nel sistema, ma non può aggiornare i file.

**Windows Installer 2.0:** È necessario impostare la [**proprietà REINSTALL**](reinstall.md) nella riga di comando quando si applica un aggiornamento di [piccole](small-updates.md) dimensioni o una patch di [aggiornamento secondaria.](minor-upgrades.md) Per le patch che non usano un tipo di azione personalizzata [51](custom-action-type-51.md) per impostare automaticamente le proprietà **REINSTALL** e [**REINSTALLMODE,**](reinstallmode.md) la proprietà **REINSTALL** deve essere impostata in modo esplicito con il *parametro CommandLine.* Impostare la **proprietà REINSTALL** per elencare le funzionalità interessate dalla patch o usare un'impostazione predefinita pratica "REINSTALL=ALL". Il valore predefinito della **proprietà REINSTALLMODE** è "omus".

**Windows Installer 3.0 e versioni successive:** A partire Windows Installer versione 3.0, la proprietà [**REINSTALL**](reinstall.md) viene configurata dal programma di installazione e non deve essere impostata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003 o Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




