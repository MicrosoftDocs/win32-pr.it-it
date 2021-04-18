---
description: Restituisce una stringa che contiene informazioni aggiuntive sull'errore relative alla voce indicizzata.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'Metodo IChain2:: ExtendedErrorInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329612"
---
# <a name="ichain2extendederrorinfo-method"></a>Metodo IChain2:: ExtendedErrorInfo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **ExtendedErrorInfo** restituisce una stringa che contiene informazioni aggiuntive sull'errore relative alla voce indicizzata.

Questo metodo è stato introdotto in capicol 2,0.

## <a name="syntax"></a>Sintassi


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in, facoltativo\]
</dt> <dd>

Oggetto **Long** che rappresenta l'indice della voce. Il valore predefinito è 1, che restituisce informazioni sull'errore per il certificato finale nella catena. **Certificates. Count** restituisce informazioni sul certificato radice della catena. 0 restituisce informazioni estese sull'errore per l'intera catena.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa che contiene le informazioni estese sull'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Catena**](chain.md)
</dt> </dl>

 

 
