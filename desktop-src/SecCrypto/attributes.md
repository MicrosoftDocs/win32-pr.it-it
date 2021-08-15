---
description: Rappresenta una raccolta di oggetti Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Oggetto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61936fff0421c43a07483fb8489cca755154a8cfbdd524da5837b12f90add969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773182"
---
# <a name="attributes-object"></a>Oggetto Attributes

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la classe [**CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto** Attributes rappresenta una raccolta di [**oggetti**](attribute.md) Attribute. Ogni [**oggetto Attribute**](attribute.md) rappresenta un singolo attributo di un messaggio.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Attributes viene usato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un [**oggetto Attribute**](attribute.md) specifico dalla raccolta.
-   Cancellare la raccolta.
-   Recupera il numero di attributi nella raccolta.
-   Recuperare un oggetto [**Attribute**](attribute.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto Attributes** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Attributes** dispone di questi metodi.



| Metodo                              | Descrizione                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Aggiungere**](attributes-add.md)       | Aggiunge un [**oggetto Attribute**](attribute.md) alla raccolta.<br/>       |
| [**Cancella**](attributes-clear.md)   | Cancella tutti gli [**oggetti Attribute**](attribute.md) dall'insieme.<br/> |
| [**Rimuovi**](attributes-remove.md) | Rimuove un [**oggetto Attribute**](attribute.md) dalla raccolta.<br/>  |



 

### <a name="properties"></a>Proprietà

**L'oggetto Attributes** ha queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](attributes-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti Attribute**](attribute.md) nella raccolta.<br/>                                                                                                                                    |
| [**Elemento**](attributes-item.md)<br/>         | Sola lettura<br/> | Recupera [**l'oggetto Attribute**](attribute.md) che rappresenta l'attributo indicizzato. Si tratta della proprietà predefinita.<br/>                                                                                             |



 

## <a name="remarks"></a>Commenti

Impossibile **creare** l'oggetto Attributes.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti di crittografia](cryptography-objects.md)
</dt> </dl>

 

 
