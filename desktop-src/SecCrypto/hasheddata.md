---
description: Fornisce la funzionalità per l'hashing di una stringa.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Oggetto HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325597"
---
# <a name="hasheddata-object"></a>Oggetto HashedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **HashedData** fornisce la funzionalità per l'hashing di una stringa.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **HashedData** viene usato per eseguire le attività seguenti:

-   Specificare la stringa di contenuto che contiene i dati di cui eseguire l'hashing.
-   Applicare un algoritmo hash specificato alla stringa di contenuto.

## <a name="members"></a>Membri

L'oggetto **HashedData** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **HashedData** dispone di questi metodi.



| Metodo                          | Descrizione                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Hash**](hasheddata-hash.md) | Crea un hash della stringa specificata.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **HashedData** dispone di queste proprietà.



| Proprietà                                             | Tipo di accesso           | Descrizione                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](hasheddata-algorithm.md)<br/> | Lettura/Scrittura<br/> | Imposta o Recupera il tipo di algoritmo di hash utilizzato.<br/>                                                                                                                     |
| [**Valore**](hasheddata-value.md)<br/>         | Sola lettura<br/>  | Recupera i dati con hash dopo le chiamate al metodo [**hash**](hasheddata-hash.md) . L'hash viene restituito in formato esadecimale. Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

Per creare l'hash di una grande quantità di dati, chiamare il metodo [**hash**](hasheddata-hash.md) per ogni pezzo di dati. L'hash di ogni porzione di dati viene concatenato alla proprietà [**value**](hasheddata-value.md) fino a quando non viene letta la proprietà. Il contenuto della proprietà **value** viene reimpostato quando viene letta la proprietà.

È possibile creare l'oggetto **HashedData** ed è sicuro per lo scripting. Il ProgID per l'oggetto **HashedData** è "CAPICOM. HashedData. 1 ".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
