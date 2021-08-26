---
description: Specifica l'algoritmo utilizzato per le operazioni di firma, avvolse e crittografia.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Oggetto Algorithm (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b52054c170cd8072bde1b742d0446732fa0b89d2be0dfc2efc66d557cdf98fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880161"
---
# <a name="algorithm-object"></a>Oggetto algoritmo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto Algorithm** specifica l'algoritmo usato per le operazioni di firma, avvolgono e crittografa.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto Algorithm** viene usato per eseguire le attività seguenti:

-   Impostare o recuperare l'algoritmo da usare.
-   Impostare o recuperare la lunghezza della chiave.

> [!Note]  
> CAPICOM tenta di usare il provider del servizio di crittografia (CSP) predefinito del sistema. Se il provider CSP non è in grado di fornire l'algoritmo richiesto o la lunghezza della chiave, CAPICOM cerca un CSP fornito da Microsoft disponibile in grado di gestire l'algoritmo richiesto e la lunghezza della chiave, in questo ordine di disponibilità: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.

 

## <a name="members"></a>Membri

**L'oggetto Algorithm** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Algorithm** ha queste proprietà.



| Proprietà                                            | Tipo di accesso           | Descrizione                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera la lunghezza della chiave.<br/>                                                                               |
| [**Nome**](algorithm-name.md)<br/>           | Lettura/Scrittura<br/> | Imposta o recupera l'algoritmo utilizzato per la firma, l'avvolsamento e la crittografia delle operazioni. Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile **creare** l'oggetto Algorithm.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| Intestazione<br/>                | <dl> <dt>Capicom.h</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
