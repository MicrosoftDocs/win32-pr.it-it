---
description: L'oggetto Product rappresenta un'istanza univoca di un prodotto annunciato, installato o sconosciuto. È possibile creare un'istanza dell'oggetto con la proprietà Product come &\# 0034; WindowsInstaller. Installer. Product (ProductCode, UserSid, context) &\# 0034;.
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
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326540"
---
# <a name="product-object"></a>Oggetto Product

L'oggetto **Product** rappresenta un'istanza univoca di un prodotto annunciato, installato o sconosciuto.

È possibile creare un'istanza dell'oggetto con la proprietà **Product** come "WindowsInstaller. Installer. Product (*ProductCode*, *UserSID*, *context*)". *UserSID* deve essere null per il contesto per computer. *UserSID* può essere null per l'utente corrente specificato, quando il contesto non è per computer. *ProductCode* e i parametri di *contesto* sono obbligatori.

## <a name="members"></a>Membri

L'oggetto **prodotto** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **prodotto** presenta questi metodi.



| Metodo                                                                 | Descrizione                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Aggiungere un disco al set di dischi registrati.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Aggiungere un'origine di rete o URL all'elenco di origine.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Cancella l'elenco di origine completo del tipo di origine specificato.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Rimuovere un disco dal set di dischi registrati dall'elenco di origine.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Rimuovere un'origine di rete o URL dall'elenco di origine.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Cancella l'ultima origine usata. Questa operazione impone la risoluzione dell'elenco di origine la volta successiva che l'origine è obbligatoria.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **Product** dispone di queste proprietà.



| Proprietà                                                      | Descrizione                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | Stato di un componente specificato per questa istanza del prodotto. <br/>                   |
| [**Context**](product-context.md)<br/>                 | Contesto di questa istanza del prodotto come valore MSIINSTALLCONTEXT. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | Stato di una funzionalità specificata per questa istanza del prodotto. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Valore di una proprietà specificata. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumera tutti i dischi multimediali per questa istanza del prodotto.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Restituisce il codice del prodotto. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Ottenere e impostare le proprietà delle informazioni sull'origine. Si tratta di una proprietà di lettura o scrittura.<br/> |
| [**Fonti**](product-sources.md)<br/>                 | Enumera tutte le origini per questa istanza del prodotto.<br/>                            |
| [**State**](product-state.md)<br/>                     | Stato di installazione del prodotto.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Restituisce il SID dell'utente, in base al quale account è disponibile questa istanza del prodotto.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




