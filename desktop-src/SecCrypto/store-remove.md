---
description: Il metodo Remove rimuove un certificato da un archivio certificati aperto. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327083"
---
# <a name="storeremove-method"></a>Store. Remove (metodo)

\[Il metodo **Remove** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Remove** rimuove un [*certificato*](../secgloss/c-gly.md) da un [*archivio certificati*](../secgloss/c-gly.md)aperto. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Certificato* \[ di in\]
</dt> <dd>

Espressione che viene risolta in un'istanza di un oggetto [**certificato**](certificate.md) da rimuovere dall'archivio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve eliminare i certificati digitali dal computer locale. Consentire ai siti Web non attendibili di eliminare i certificati digitali costituisce un rischio per la sicurezza. Viene visualizzata una finestra di dialogo in cui viene chiesto se il sito Web può eliminare i certificati quando questo metodo viene chiamato per la prima volta. Se si consente all'applicazione di eliminare i certificati e selezionare "non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per gli script che eliminano i certificati all'interno di tale dominio. Tuttavia, gli script esterni al dominio che tentano di eliminare i certificati continueranno a causare la visualizzazione di questa finestra di dialogo. Se non si consente allo script di eliminare i certificati e selezionare "non visualizzare più questa finestra di dialogo", gli script all'interno di tale dominio verranno automaticamente rifiutati la possibilità di eliminare i certificati.

 

Quando si elimina un certificato da un archivio, è necessario innanzitutto eliminare la chiave privata associata al certificato.

Se l'archivio non è aperto con l'autorizzazione di lettura/scrittura, questo metodo ha esito negativo. Sebbene questo metodo possa essere utilizzato con gli archivi di memoria, le modifiche apportate a un archivio di memoria non vengono rese permanente quando l'archivio viene chiuso.

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

 

 
