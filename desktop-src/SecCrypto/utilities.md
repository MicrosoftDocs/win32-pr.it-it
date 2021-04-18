---
description: Fornisce funzionalità per la generazione di numeri casuali, le conversioni e la codifica e la decodifica da Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Utilità (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331261"
---
# <a name="utilities-object"></a>Utilità (oggetto)

\[L'oggetto **Utilities** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

L'oggetto **Utilities** fornisce funzionalità per la generazione di numeri casuali, le conversioni e la codifica e la decodifica da Base64.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **Utilities** viene utilizzato per eseguire le attività seguenti:

-   Codificare una stringa come base64 o decodificare una stringa da Base64.
-   Converte una stringa con pacchetto binario in una matrice di byte e viceversa.
-   Converte una stringa con pacchetto binario in una stringa esadecimale e viceversa.
-   Genera un numero casuale protetto.
-   Converte l'ora locale in ora UTC (ora di Greenwich) e viceversa.

## <a name="members"></a>Membri

L'oggetto **Utilities** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **Utilities** presenta questi metodi.



| Metodo                                                               | Descrizione                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Base64Decode**](utilities-base64decode.md)                       | Decodifica una stringa da Base64.<br/>                                     |
| [**Base64Encode**](utilities-base64encode.md)                       | Codifica una stringa come Base64.<br/>                                       |
| [**BinaryStringToByteArray**](utilities-binarystringtobytearray.md) | Converte una stringa con pacchetto binario in una matrice di byte.<br/>             |
| [**BinaryToHex**](utilities-binarytohex.md)                         | Converte una stringa con pacchetto binario in una stringa esadecimale.<br/>          |
| [**ByteArrayToBinaryString**](utilities-bytearraytobinarystring.md) | Converte una matrice di byte in una stringa con pacchetto binario.<br/>             |
| [**GetRandom**](utilities-getrandom.md)                             | Genera un numero casuale protetto.<br/>                                 |
| [**HexToBinary**](utilities-hextobinary.md)                         | Converte una stringa esadecimale in una stringa con pacchetto binario.<br/>          |
| [**LocalTimeToUTCTime**](utilities-localtimetoutctime.md)           | Converte l'ora locale del computer nell'ora UTC (Coordinated Universal Time).<br/> |
| [**UTCTimeToLocalTime**](utilities-utctimetolocaltime.md)           | Converte l'ora UTC (Coordinated Universal Time) nell'ora locale del computer.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **Utilities** ed è sicuro per lo scripting. Il ProgID per l'oggetto **Utilities** è capicom. Utilities. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




