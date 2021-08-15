---
description: Decodifica una stringa da base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Metodo Utilities.Base64Decode
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
ms.openlocfilehash: 727aa28edf14a038ec4667d1705a82f6fd3a2c3bc4a4c4e5ba0e6bf743d143d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896630"
---
# <a name="utilitiesbase64decode-method"></a>Metodo Utilities.Base64Decode

\[Il **metodo Base64Decode** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.\]

Il **metodo Base64Decode** decodifica una stringa da base64.

## <a name="syntax"></a>Sintassi


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodedString* \[ Pollici\]
</dt> <dd>

Stringa con codifica Base64 da decodificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa decodificata.

## <a name="remarks"></a>Commenti

La codifica Base64 è lo schema usato per trasmettere dati binari. Base64 elabora i dati come gruppi a 24 bit, mappando questi dati a quattro caratteri codificati. La codifica Base64 viene talvolta definita codifica da 3 a 4. Ogni 6 bit del gruppo a 24 bit viene usato come indice in una tabella di mapping (alfabeto base64) per ottenere un carattere per i dati codificati. I dati codificati hanno lunghezze di riga limitate a 76 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Utilità**](utilities.md)
</dt> </dl>

 

 




