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
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332745"
---
# <a name="attribute-object"></a>Attribute - oggetto

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]

L'oggetto **attribute** rappresenta un singolo attributo autenticato.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **attributo** viene utilizzato per eseguire le attività seguenti:

-   Imposta o Recupera il nome del CAPICOM dell'attributo.
-   Impostare o recuperare il valore dell'attributo, ad esempio l'ora di firma, il nome del documento firmato o una descrizione del documento firmato.

## <a name="members"></a>Membri

L'oggetto **attributo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **attributo** dispone di queste proprietà.



| Proprietà                                    | Tipo di accesso           | Descrizione                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Nome**](attribute-name.md)<br/>   | Lettura/Scrittura<br/> | Imposta o Recupera il nome del CAPICOM dell'attributo. Si tratta della proprietà predefinita.<br/> |
| [**Valore**](attribute-value.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il valore dell'attributo.<br/>                                      |



 

## <a name="remarks"></a>Commenti

L'oggetto **attributo** può essere creato ed è sicuro per lo scripting. Il ProgID per l'oggetto **attributo** è capicom. Attributo. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
