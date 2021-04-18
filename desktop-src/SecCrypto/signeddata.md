---
description: Fornisce proprietà e metodi per stabilire il contenuto da firmare con una firma digitale, per firmare o cofirmare i dati in modo digitale e per verificare la firma digitale dei dati firmati. Il messaggio firmato è in \# formato PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Oggetto SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325144"
---
# <a name="signeddata-object"></a>Oggetto SignedData

\[L'oggetto **SignedData** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **SignedData** fornisce proprietà e metodi per stabilire il contenuto da firmare con una [*firma digitale*](../secgloss/d-gly.md), per firmare o cofirmare i dati in modo digitale e per verificare la firma digitale dei dati firmati. Il messaggio firmato è in \# formato PKCS 7.

Una firma dati, se verificata, dimostra l'associazione tra un firmatario e i dati e indica che i dati non sono stati modificati in alcun modo dopo la creazione della firma.

## <a name="members"></a>Membri

L'oggetto **SignedData** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SignedData** dispone di questi metodi.



| Metodo                              | Descrizione                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**CoSign**](signeddata-cosign.md) | Firma un messaggio già firmato.<br/>                       |
| [**Sign**](signeddata-sign.md)     | Crea una firma digitale sul contenuto da firmare.<br/> |
| [**Verificare**](signeddata-verify.md) | Determina la validità di una firma o di firme.<br/>    |



 

### <a name="properties"></a>Proprietà

L'oggetto **SignedData** dispone di queste proprietà.



| Proprietà                                                   | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](signeddata-certificates.md)<br/> | Sola lettura<br/>  | Recupera la raccolta di [**certificati**](certificates.md) dei dati firmati.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Contenuto**](signeddata-content.md)<br/>           | Lettura/Scrittura<br/> | Dati da firmare. Questa proprietà deve essere inizializzata prima che venga chiamato il metodo [**Sign**](signeddata-sign.md) .<br/> Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e tutte le firme associate all'oggetto prima della modifica della proprietà vengono perse.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Firmatari**](signeddata-signers.md)<br/>           | Sola lettura<br/>  | Recupera la raccolta di [**firmatari**](signers.md) che rappresenta gli autori della firma dei dati.<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **SignedData** ed è sicuro per lo scripting. Il ProgID per l'oggetto **SignedData** è capicom. SignedData. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
