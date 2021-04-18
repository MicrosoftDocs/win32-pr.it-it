---
description: Genera un numero casuale sicuro utilizzando il provider del servizio di crittografia (CSP) predefinito.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities. GetRandom, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327884"
---
# <a name="utilitiesgetrandom-method"></a>Utilities. GetRandom, metodo

\[Il metodo **GetRandom** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

Il metodo **GetRandom** genera un numero casuale sicuro usando il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) predefinito.

## <a name="syntax"></a>Sintassi


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Lunghezza* \[ in, facoltativo\]
</dt> <dd>

Lunghezza, in byte, del numero casuale da creare. Il valore predefinito è 8 byte.

</dd> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica il tipo di codifica da utilizzare per il numero casuale generato. Il valore predefinito è CAPICOM \_ Encode \_ Binary. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Encode \_ any**</dt> </dl>          | Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64. Introdotta in capicol 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Codifica Base64 per CAPICOM \_**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_codificare il \_ file binario di CAPICOM**</dt> </dl> | I dati vengono salvati come una sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

*Lunghezza* in byte del numero generato casualmente, con la codifica specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Utilità**](utilities.md)
</dt> </dl>

 

 
