---
description: Fornisce funzionalità per l'hashing di una stringa.
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
ms.openlocfilehash: c61d52e7621acffb76df5bcb05693efb48c695c15e79d1f0a45523a0f0087c6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006449"
---
# <a name="hasheddata-object"></a>Oggetto HashedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto HashedData** fornisce funzionalità per l'hashing di una stringa.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto HashedData** viene usato per eseguire le attività seguenti:

-   Specificare la stringa di contenuto che contiene i dati di cui eseguire l'hashing.
-   Applica un algoritmo hash specificato alla stringa di contenuto.

## <a name="members"></a>Membri

**L'oggetto HashedData** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto HashedData** dispone di questi metodi.



| Metodo                          | Descrizione                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Hash**](hasheddata-hash.md) | Crea un hash della stringa specificata.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto HashedData** ha queste proprietà.



| Proprietà                                             | Tipo di accesso           | Descrizione                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](hasheddata-algorithm.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera il tipo di algoritmo hash utilizzato.<br/>                                                                                                                     |
| [**Valore**](hasheddata-value.md)<br/>         | Sola lettura<br/>  | Recupera i dati con hash dopo le chiamate riuscite al [**metodo Hash.**](hasheddata-hash.md) L'hash viene restituito in formato esadecimale. Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

Per creare l'hash di una grande quantità di dati, chiamare il [**metodo Hash**](hasheddata-hash.md) per ogni dato. L'hash di ogni dato viene concatenato alla [**proprietà Value**](hasheddata-value.md) fino a quando la proprietà non viene letta. Il contenuto della **proprietà Value** viene reimpostato quando la proprietà viene letta.

**L'oggetto HashedData** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto HashedData** è "CAPICOM. HashedData.1".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
