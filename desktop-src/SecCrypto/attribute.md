---
description: Rappresenta un singolo attributo autenticato.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute - oggetto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3e07c771a34e89cfbcbba5695450e195ef55482e0a27bee008f3ea8251bf8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879871"
---
# <a name="attribute-object"></a>Attribute - oggetto

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/previous-versions/windows/)\]

**L'oggetto Attribute** rappresenta un singolo attributo autenticato.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Attribute viene usato per eseguire le attività seguenti:

-   Impostare o recuperare il nome CAPICOM dell'attributo.
-   Impostare o recuperare il valore dell'attributo, ad esempio l'ora di firma, il nome del documento firmato o una descrizione del documento firmato.

## <a name="members"></a>Membri

**L'oggetto Attribute** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Attribute** ha queste proprietà.



| Proprietà                                    | Tipo di accesso           | Descrizione                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Nome**](attribute-name.md)<br/>   | Lettura/Scrittura<br/> | Imposta o recupera il nome CAPICOM dell'attributo. Si tratta della proprietà predefinita.<br/> |
| [**Valore**](attribute-value.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera il valore dell'attributo.<br/>                                      |



 

## <a name="remarks"></a>Commenti

**L'oggetto Attribute** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto Attribute** è CAPICOM. Attribute.1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
