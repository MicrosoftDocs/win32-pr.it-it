---
title: Proprietà dell'ambiente ITsSbClientConnection
description: Recupera un oggetto che contiene informazioni sull'ambiente che ospita il computer di destinazione.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà ambiente
- Servizi Desktop remoto Proprietà ambiente, interfaccia ITsSbClientConnection
- Interfaccia ITsSbClientConnection Servizi Desktop remoto, proprietà Environment
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477723"
---
# <a name="itssbclientconnectionenvironment-property"></a>Proprietà ITsSbClientConnection:: Environment

Recupera un oggetto che contiene informazioni sull'ambiente che ospita il computer di destinazione. Ad esempio, in uno scenario di desktop virtuale, questo oggetto contiene informazioni sul computer che ospita la macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un puntatore a un oggetto di ambiente [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un valore **HRESULT** che indica l'errore. I valori possibili includono, ma non sono limitati a, quelli nell'elenco seguente.

<dl> <dt>

\_puntatore E
</dt> <dd>

L'ambiente non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un plug-in di orchestrazione può chiamare questo metodo per recuperare le informazioni sull'ambiente di una macchina virtuale di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





