---
description: Decodifica una stringa da Base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Utilities. Base64Decode, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327995"
---
# <a name="utilitiesbase64decode-method"></a>Utilities. Base64Decode, metodo

\[Il metodo **Base64Decode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

Il metodo **Base64Decode** decodifica una stringa da Base64.

## <a name="syntax"></a>Sintassi


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodedString* \[ in\]
</dt> <dd>

Stringa con codifica base64 da decodificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa decodificata.

## <a name="remarks"></a>Commenti

La codifica Base64 è lo schema utilizzato per la trasmissione di dati binari. Base64 elabora i dati come gruppi a 24 bit, eseguendo il mapping di questi dati a quattro caratteri codificati. La codifica Base64 viene a volte definita codifica da 3 a 4. Ogni 6 bit del gruppo a 24 bit viene utilizzato come indice in una tabella di mapping (alfabeto Base64) per ottenere un carattere per i dati codificati. I dati codificati hanno lunghezze di riga limitate a 76 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Utilità**](utilities.md)
</dt> </dl>

 

 




