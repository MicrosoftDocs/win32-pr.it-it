---
description: Specifica l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Oggetto Algorithm (CAPICOM. h)
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
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324595"
---
# <a name="algorithm-object"></a>Oggetto Algorithm

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **Algorithm** specifica l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **Algorithm** viene utilizzato per eseguire le attività seguenti:

-   Impostare o recuperare l'algoritmo da utilizzare.
-   Imposta o recupera la lunghezza della chiave.

> [!Note]  
> CAPICOM tenta di utilizzare il provider del servizio di crittografia (CSP) predefinito di sistema. Se il CSP non è in grado di fornire l'algoritmo o la lunghezza della chiave richiesti, CAPICOM Cerca un provider di servizi CSP fornito da Microsoft in grado di gestire l'algoritmo e la lunghezza della chiave richiesti, in questo ordine di disponibilità: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.

 

## <a name="members"></a>Membri

L'oggetto **algoritmo** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **Algorithm** dispone di queste proprietà.



| Proprietà                                            | Tipo di accesso           | Descrizione                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera la lunghezza della chiave.<br/>                                                                               |
| [**Nome**](algorithm-name.md)<br/>           | Lettura/Scrittura<br/> | Imposta o recupera l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni. Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **algoritmo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| Intestazione<br/>                | <dl> <dt>CAPICOM. h</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
