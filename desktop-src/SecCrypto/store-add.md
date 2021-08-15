---
description: Aggiunge un oggetto Certificato a un archivio certificati aperto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Metodo Store.Add
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
ms.openlocfilehash: f90d95184fd789530831628cb6e121e32ce258d4541769c47926d2fb46eb710c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897936"
---
# <a name="storeadd-method"></a>Metodo Store.Add

\[Il **metodo** Add è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Add** aggiunge un oggetto [**Certificate**](certificate.md) a un archivio [*certificati aperto.*](../secgloss/c-gly.md) Questo metodo può essere utilizzato solo con un archivio aperto con autorizzazione di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Certificato* \[ Pollici\]
</dt> <dd>

Espressione che viene risolta in [**un oggetto Certificate**](certificate.md) da aggiungere all'archivio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato in un archivio di sistema da uno script Web, lo script deve accedere ai certificati digitali nel computer locale. Se si consente allo script di accedere ai certificati digitali, anche il sito Web da cui viene eseguito lo script avrà accesso alle informazioni personali archiviate nei certificati. La prima volta che questo metodo viene chiamato da un dominio specifico, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito.

 

Se l'archivio non è aperto in modalità lettura/scrittura, questo metodo ha esito negativo. Anche se questo metodo può essere usato con gli archivi di memoria, tutte le modifiche apportate a un archivio di memoria non vengono rese persistenti quando l'archivio viene chiuso.

Se il certificato aggiunto all'archivio è uguale a quello già presente, il metodo **Add** elimina il certificato esistente dall'archivio e quindi aggiunge il nuovo certificato. Il nuovo certificato eredita le proprietà dal certificato esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archiviazione**](store.md)
</dt> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
