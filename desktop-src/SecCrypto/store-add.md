---
description: Aggiunge un oggetto certificato a un archivio certificati aperto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330267"
---
# <a name="storeadd-method"></a>Store. Add (metodo)

\[Il metodo **Add** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Add** aggiunge un oggetto [**certificato**](certificate.md) a un [*archivio certificati*](../secgloss/c-gly.md)aperto. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Certificato* \[ di in\]
</dt> <dd>

Espressione che viene risolta in un oggetto [**certificato**](certificate.md) da aggiungere all'archivio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato in un archivio di sistema da uno script Web, lo script deve accedere ai certificati digitali nel computer locale. Se si consente allo script di accedere ai certificati digitali, il sito Web da cui viene eseguito lo script otterrà anche l'accesso a tutte le informazioni personali archiviate nei certificati. La prima volta che questo metodo viene chiamato da un particolare dominio, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito.

 

Se l'archivio non è aperto in modalità di lettura/scrittura, questo metodo ha esito negativo. Sebbene questo metodo possa essere utilizzato con gli archivi di memoria, le modifiche apportate a un archivio di memoria non vengono rese permanente quando l'archivio viene chiuso.

Se il certificato da aggiungere all'archivio è identico a quello già presente, il metodo **Add** Elimina il certificato esistente dall'archivio e quindi aggiunge il nuovo certificato. Il nuovo certificato eredita le proprietà dal certificato esistente.

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

 

 
