---
description: Il metodo di importazione copia in un certificato aperto archivia il contenuto di un archivio certificati precedentemente esportato. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331264"
---
# <a name="storeimport-method"></a>Store. Import (metodo)

\[Il metodo di **importazione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo di **importazione** copia in un [*certificato aperto archivia*](../secgloss/c-gly.md) il contenuto di un archivio certificati precedentemente esportato. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodedStore* \[ in\]
</dt> <dd>

Stringa che contiene i certificati codificati da importare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve accedere ai certificati digitali sul computer locale. Se si consente allo script di accedere ai certificati digitali, il sito Web da cui viene eseguito lo script otterrà anche l'accesso a tutte le informazioni personali archiviate nei certificati. La prima volta che questo metodo viene chiamato da un particolare dominio, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito.

 

Se l'archivio non viene aperto con l'autorizzazione di lettura/scrittura, questo metodo ha esito negativo. Sebbene questo metodo possa essere utilizzato con gli archivi di memoria, le modifiche apportate a un archivio di memoria non vengono rese permanente quando l'archivio viene chiuso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
