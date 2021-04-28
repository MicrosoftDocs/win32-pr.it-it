---
description: 'Oggetto NoticeNumbers: rappresenta una raccolta di oggetti Extension.'
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Oggetto NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090759"
---
# <a name="noticenumbers-object"></a>Oggetto NoticeNumbers

\[**L'oggetto NoticeNumbers** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Per altre informazioni, vedere [**Qualificatore.**](qualifier.md)\]

**L'oggetto NoticeNumbers** rappresenta una raccolta di [**oggetti Extension.**](extension.md) Ogni [**oggetto Extension**](extension.md) rappresenta un numero di avviso dell'utente.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto NoticeNumbers** viene usato per eseguire le attività seguenti:

-   Recupera il numero di [**oggetti Extension**](extension.md) nella raccolta.
-   Recuperare un oggetto [**Extension**](extension.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto NoticeNumbers** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto NoticeNumbers** ha queste proprietà.



| Proprietà                                              | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](noticenumbers-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti Extension**](extension.md) nella raccolta.<br/>                                                                                                                                    |
| [**Elemento**](noticenumbers-item.md)<br/>         | Sola lettura<br/> | Recupera [**l'oggetto Extension**](extension.md) che rappresenta il numero di avviso indicizzato della raccolta.<br/> Si tratta della proprietà predefinita.<br/>                                                            |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto NoticeNumbers.**

L'oggetto NoticeNumbers viene usato nella [**proprietà Qualifier.NoticeNumbers.**](qualifier-noticenumbers.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
