---
description: Il metodo Remove rimuove un certificato da un archivio certificati aperto. Questo metodo può essere usato solo con un archivio aperto con autorizzazione di lettura/scrittura.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Metodo Store.Remove
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
ms.openlocfilehash: 0f3700c8f61861987bc5311a637722955c62a1c6ad1572c7628d9ab9e0f5c76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897686"
---
# <a name="storeremove-method"></a>Metodo Store.Remove

\[Il **metodo Remove** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Remove** rimuove un certificato [*da*](../secgloss/c-gly.md) un archivio [*certificati aperto.*](../secgloss/c-gly.md) Questo metodo può essere usato solo con un archivio aperto con autorizzazione di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Certificato* \[ Pollici\]
</dt> <dd>

Espressione che si risolve in un'istanza di un [**oggetto Certificate**](certificate.md) da rimuovere dall'archivio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve eliminare i certificati digitali dal computer locale. Consentire ai siti Web non attendibili di eliminare i certificati digitali è un rischio per la sicurezza. Quando questo metodo viene chiamato per la prima volta, viene visualizzata una finestra di dialogo che chiede se il sito Web può eliminare i certificati. Se si consente all'applicazione di eliminare i certificati e si seleziona "Non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per qualsiasi script che elimina i certificati all'interno di tale dominio. Tuttavia, gli script esterni a tale dominio che tentano di eliminare i certificati causeranno comunque la visualizzazione di questa finestra di dialogo. Se non si consente allo script di eliminare i certificati e si seleziona "Non visualizzare più questa finestra di dialogo", agli script all'interno di tale dominio verrà automaticamente negata la possibilità di eliminare i certificati.

 

Quando si elimina un certificato da un archivio, è prima necessario eliminare la chiave privata associata al certificato.

Se l'archivio non è aperto con autorizzazione di lettura/scrittura, questo metodo ha esito negativo. Anche se questo metodo può essere usato con gli archivi di memoria, tutte le modifiche apportate a un archivio di memoria non vengono rese persistenti quando l'archivio viene chiuso.

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

 

 
