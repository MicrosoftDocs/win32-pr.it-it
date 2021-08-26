---
description: L'oggetto Patch rappresenta un'istanza univoca di una patch registrata o applicata. È possibile creare un'istanza dell'oggetto con la proprietà Patch &\# 0034; WindowsInstaller.Installer.Patch(PatchCode, ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Oggetto Patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9e337af735a39312cb5aa740283cb8b4d8b508be33f28c302788a1207f89472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074841"
---
# <a name="patch-object"></a>Oggetto Patch

**L'oggetto Patch** rappresenta un'istanza univoca di una patch registrata o applicata.

È possibile creare un'istanza dell'oggetto con la proprietà **Patch** come "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)". Per un contesto del computer, *il parametro UserSid* deve essere una stringa vuota. ProductCode *può* essere impostato su una stringa vuota per le patch registrate solo e non ancora applicate ad alcun prodotto. ProductCode *può essere* impostato su una stringa vuota solo durante la lettura o l'aggiornamento delle informazioni dell'elenco di origine di una patch.

## <a name="members"></a>Membri

**L'oggetto Patch** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Patch** dispone di questi metodi.



| Metodo                                                               | Descrizione                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Aggiungere un disco al set di dischi registrati.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Aggiungere un'origine di rete o URL all'elenco di origine. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Cancella l'elenco di origine completo del tipo specificato di origini.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Rimuovere un disco dal set di dischi registrati dall'elenco di origine. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Rimuovere un'origine di rete o URL dall'elenco di origine.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Cancella l'ultima origine usata dall'elenco di origine. In questo modo viene forzata la risoluzione dell'elenco di origine alla successiva richiesta dell'origine.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto Patch** ha queste proprietà.



| Proprietà                                                  | Descrizione                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Context**](patch-context.md)<br/>               | Il contesto di questa istanza della patch è un valore MSIINSTALLCONTEXT.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Enumera tutti i dischi multimediali per questa istanza di patch.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Restituisce il codice della patch.<br/>                                                                         |
| [**Proprietà Patch**](patch-patchproperty.md)<br/>   | Ottiene informazioni sulle proprietà relative a una patch specifica applicata a un'istanza specifica del prodotto.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Restituisce il codice prodotto.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Ottiene e imposta le proprietà delle informazioni di origine. Si tratta di una proprietà di lettura o scrittura.<br/>              |
| [**recenti**](patch-sources.md)<br/>               | Enumera tutte le origini per questa istanza di patch.<br/>                                             |
| [**Stato**](patch-state.md)<br/>                   | Stato di installazione della patch.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Restituisce il SID utente, nell'account in cui è disponibile questa istanza della patch.<br/>                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Esempi di script del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




