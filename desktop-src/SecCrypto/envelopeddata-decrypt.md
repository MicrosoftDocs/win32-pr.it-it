---
description: Decrittografa il contenuto in busta.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Metodo EnvelopedData. Decrypt
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
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327897"
---
# <a name="envelopeddatadecrypt-method"></a>Metodo EnvelopedData. Decrypt

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **Decrypt** decrittografa il contenuto in busta digitale. La decrittografia viene eseguita se il destinatario del messaggio ha accesso alla [*chiave privata*](../secgloss/p-gly.md) associata a una delle [*chiavi pubbliche*](../secgloss/p-gly.md) usate per la busta del messaggio. La chiamata al metodo **Decrypt** Reimposta lo [*stato*](../secgloss/s-gly.md) dell'oggetto. Se il metodo **Decrypt** ha esito positivo, la proprietà [**Content**](envelopeddata-content.md) dell'oggetto [**EnvelopedData**](envelopeddata.md) viene impostata sul messaggio in testo non crittografato.

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnvelopedMessage* \[ in\]
</dt> <dd>

Stringa che contiene i dati in busta da decrittografare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I dati decrittografati diventeranno il valore della proprietà [**Content**](envelopeddata-content.md) per l'oggetto [**EnvelopedData**](envelopeddata.md) .

Se l'utente di questo metodo non ha accesso a una chiave privata che corrisponde a una delle chiavi pubbliche usate per la busta del messaggio, il metodo ha esito negativo. Questo metodo avrà esito negativo se il certificato per la chiave privata associata non si trova nell'archivio personale del computer locale o dell'utente corrente.

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve usare la [*chiave privata*](../secgloss/p-gly.md) per decrittografare i dati. Consentire ai siti Web non attendibili di usare la chiave privata costituisce un rischio per la sicurezza. Una finestra di dialogo in cui viene chiesto se il sito Web può utilizzare la chiave privata viene visualizzata quando questo metodo viene chiamato per la prima volta. Se si consente allo script di usare la chiave privata e selezionare "non visualizzare più questo messaggio", la finestra di dialogo non verrà più visualizzata per gli script che usano la chiave privata per decrittografare i dati all'interno del dominio. Tuttavia, gli script all'esterno del dominio che tentano di usare la chiave privata per decrittografare i dati continueranno a causare la visualizzazione di questa finestra di dialogo. Se non si consente allo script di usare la chiave privata e selezionare "non visualizzare più questo messaggio", gli script all'interno di tale dominio verranno automaticamente rifiutati la possibilità di usare la chiave privata per decrittografare i dati.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
