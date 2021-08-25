---
description: Decrittografa il contenuto in busta.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Metodo EnvelopedData.Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f1c754e23977ac9c7af7f4fd3feaade13c928e9522a2285102a095fff4740b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874261"
---
# <a name="envelopeddatadecrypt-method"></a>Metodo EnvelopedData.Decrypt

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il metodo **Decrypt** decrittografa il contenuto in busta. La decrittografia viene eseguita se il [](../secgloss/p-gly.md) destinatario del messaggio [](../secgloss/p-gly.md) ha accesso alla chiave privata associata a una delle chiavi pubbliche usate per l'ambiente del messaggio. La chiamata **al metodo Decrypt** reimposta lo [*stato*](../secgloss/s-gly.md) dell'oggetto. Se il **metodo Decrypt** ha esito positivo, la [**proprietà Content**](envelopeddata-content.md) dell'oggetto [**EnvelopedData**](envelopeddata.md) viene impostata sul messaggio di testo non crittografato.

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnvelopedMessage* \[ Pollici\]
</dt> <dd>

Stringa contenente i dati in busta da decrittografare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I dati decrittografati diventano [**il valore della**](envelopeddata-content.md) proprietà Content per [**l'oggetto EnvelopedData.**](envelopeddata.md)

Se l'utente di questo metodo non ha accesso a una chiave privata che corrisponde a una delle chiavi pubbliche usate per l'ambiente del messaggio, il metodo ha esito negativo. Questo metodo avrà esito negativo se il certificato per la chiave privata associata non si trova nell'archivio MY del computer locale o nell'archivio MY dell'utente corrente.

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve usare la [*chiave privata*](../secgloss/p-gly.md) per decrittografare i dati. Consentire ai siti Web non attendibili di usare la chiave privata è un rischio per la sicurezza. Quando questo metodo viene chiamato per la prima volta, viene visualizzata una finestra di dialogo in cui viene chiesto se il sito Web può usare la chiave privata. Se si consente allo script di usare la chiave privata e si seleziona "Non chiedere più questo", la finestra di dialogo non verrà più visualizzata per gli script che usano la chiave privata per decrittografare i dati all'interno del dominio. Tuttavia, gli script esterni a tale dominio che tentano di usare la chiave privata per decrittografare i dati causeranno comunque la visualizzazione di questa finestra di dialogo. Se non si consente allo script di usare la chiave privata e si seleziona "Non chiedere più questo", agli script all'interno di tale dominio verrà automaticamente rifiutata la possibilità di usare la chiave privata per decrittografare i dati.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
