---
description: L'oggetto patch rappresenta un'istanza univoca di una patch che è stata registrata o applicata. È possibile creare un'istanza dell'oggetto con la proprietà patch come &\# 0034; WindowsInstaller. Installer. patch (PatchCode, ProductCode, UserSid, context) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch (oggetto)
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
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325025"
---
# <a name="patch-object"></a>Patch (oggetto)

L'oggetto **patch** rappresenta un'istanza univoca di una patch che è stata registrata o applicata.

È possibile creare un'istanza dell'oggetto con la proprietà **patch** come "WindowsInstaller. Installer. patch (*PatchCode*, *ProductCode*, *UserSID*, *context*)". Per un contesto macchina, il parametro *UserSID* deve essere una stringa vuota. *ProductCode* può essere impostato su una stringa vuota per le patch registrate solo e non ancora applicate a un prodotto. *ProductCode* può essere impostato su una stringa vuota solo leggendo o aggiornando le informazioni dell'elenco di origine di una patch.

## <a name="members"></a>Membri

L'oggetto **patch** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **patch** presenta questi metodi.



| Metodo                                                               | Descrizione                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Aggiungere un disco al set di dischi registrati.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Aggiungere un'origine di rete o URL all'elenco di origine. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Cancella l'elenco di origine completo del tipo di origine specificato.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Rimuovere un disco dal set di dischi registrati dall'elenco di origine. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Rimuovere un'origine di rete o URL dall'elenco di origine.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Cancella l'ultima origine utilizzata dall'elenco di origine. Questa operazione impone la risoluzione dell'elenco di origine la volta successiva che l'origine è obbligatoria.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **patch** presenta queste proprietà.



| Proprietà                                                  | Descrizione                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Context**](patch-context.md)<br/>               | Il contesto di questa istanza di patch è un valore MSIINSTALLCONTEXT.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Enumera tutti i dischi multimediali per questa istanza della patch.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Restituisce il codice della patch.<br/>                                                                         |
| [**PatchProperty**](patch-patchproperty.md)<br/>   | Ottiene le informazioni sulle proprietà di una patch specifica applicata a un'istanza specifica del prodotto.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Restituisce il codice del prodotto.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Ottiene e imposta le proprietà delle informazioni sull'origine. Si tratta di una proprietà di lettura o scrittura.<br/>              |
| [**Fonti**](patch-sources.md)<br/>               | Enumera tutte le origini per questa istanza della patch.<br/>                                             |
| [**State**](patch-state.md)<br/>                   | Stato di installazione della patch.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Restituisce il SID dell'utente, nell'account in cui è disponibile questa istanza di patch.<br/>                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




