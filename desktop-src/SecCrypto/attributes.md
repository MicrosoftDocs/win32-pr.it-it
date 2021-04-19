---
description: Rappresenta una raccolta di oggetti attributo.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Oggetto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326530"
---
# <a name="attributes-object"></a>Oggetto Attributes

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **Attributes** rappresenta una raccolta di oggetti [**attribute**](attribute.md) . Ogni oggetto [**attributo**](attribute.md) rappresenta un singolo attributo di un messaggio.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **Attributes** viene utilizzato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un oggetto [**attributo**](attribute.md) specifico dalla raccolta.
-   Cancellare la raccolta.
-   Recuperare il numero di attributi nella raccolta.
-   Recuperare un oggetto [**attributo**](attribute.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **Attributes** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Attributes** presenta questi metodi.



| Metodo                              | Descrizione                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Aggiungere**](attributes-add.md)       | Aggiunge un oggetto [**attributo**](attribute.md) alla raccolta.<br/>       |
| [**Deselezionare**](attributes-clear.md)   | Cancella tutti gli oggetti [**attributo**](attribute.md) dalla raccolta.<br/> |
| [**Rimuovi**](attributes-remove.md) | Rimuove un oggetto [**attributo**](attribute.md) dalla raccolta.<br/>  |



 

### <a name="properties"></a>Proprietà

L'oggetto **Attributes** dispone di queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](attributes-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti [**attributo**](attribute.md) nell'insieme.<br/>                                                                                                                                    |
| [**Elemento**](attributes-item.md)<br/>         | Sola lettura<br/> | Recupera l'oggetto [**attributo**](attribute.md) che rappresenta l'attributo indicizzato. Si tratta della proprietà predefinita.<br/>                                                                                             |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **Attributes** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Cryptography](cryptography-objects.md)
</dt> </dl>

 

 
