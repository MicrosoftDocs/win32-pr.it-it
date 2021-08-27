---
description: L'oggetto Product rappresenta un'istanza univoca di un prodotto annunciato, installato o sconosciuto. È possibile creare un'istanza dell'oggetto con la proprietà Product &\# 0034; WindowsInstaller.Installer.Product(ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Oggetto Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff05a2f89244da09caa6cd3b26fc4b5d9cdbec95c0fcc3098fddf0c39dc68519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627674"
---
# <a name="product-object"></a>Oggetto Product

**L'oggetto Product** rappresenta un'istanza univoca di un prodotto annunciato, installato o sconosciuto.

È possibile creare un'istanza dell'oggetto con la proprietà **Product** come "WindowsInstaller.Installer.Product(*ProductCode,* *UserSid,* *Context*)". *UserSid* deve essere NULL per il contesto per computer. *UserSid può* essere Null per l'utente corrente specificato, quando il contesto non è per computer. *I parametri ProductCode* *e Context* sono obbligatori.

## <a name="members"></a>Membri

**L'oggetto Product** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Product** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Aggiungere un disco al set di dischi registrati.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Aggiungere un'origine di rete o URL all'elenco di origine.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Cancella l'elenco di origine completo del tipo specificato di origini.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Rimuovere un disco dal set di dischi registrati dall'elenco di origine.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Rimuovere un'origine di rete o URL dall'elenco di origine.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Cancella l'ultima origine usata. In questo modo viene forzata la risoluzione dell'elenco di origine alla successiva richiesta dell'origine.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto Product** ha queste proprietà.



| Proprietà                                                      | Descrizione                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | Stato di un componente specificato per questa istanza del prodotto. <br/>                   |
| [**Contesto**](product-context.md)<br/>                 | Contesto di questa istanza del prodotto come valore MSIINSTALLCONTEXT. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | Stato di una funzionalità specificata per questa istanza del prodotto. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Valore di una proprietà specificata. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumera tutti i dischi multimediali per questa istanza del prodotto.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Restituisce il codice del prodotto. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Ottenere e impostare le proprietà delle informazioni di origine. Si tratta di una proprietà di lettura o scrittura.<br/> |
| [**recenti**](product-sources.md)<br/>                 | Enumera tutte le origini per questa istanza del prodotto.<br/>                            |
| [**Stato**](product-state.md)<br/>                     | Stato di installazione del prodotto.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Restituisce il SID utente, in base al quale è disponibile questa istanza del prodotto.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Esempi di scripting del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




