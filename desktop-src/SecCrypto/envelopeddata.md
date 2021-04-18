---
description: L'oggetto EnvelopedData fornisce proprietà e metodi per l'inviluppo dei dati per la privacy mediante crittografia.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Oggetto EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327092"
---
# <a name="envelopeddata-object"></a>Oggetto EnvelopedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **EnvelopedData** fornisce proprietà e metodi per l'inviluppo dei dati per la privacy mediante crittografia. Per la busta dei dati, viene generata una chiave crittografica della sessione. Tale [*chiave di sessione*](../secgloss/s-gly.md) viene quindi crittografata per ogni destinatario desiderato utilizzando la [*chiave pubblica*](../secgloss/p-gly.md) di quel destinatario previsto dal certificato del destinatario. I dati crittografati e il set di chiavi di sessione crittografati possono essere inviati a tutti i destinatari desiderati. Il messaggio generato è in \# formato PKCS 7.

## <a name="members"></a>Membri

L'oggetto **EnvelopedData** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **EnvelopedData** dispone di questi metodi.



| Metodo                                   | Descrizione                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Decrypt**](envelopeddata-decrypt.md) | Decrittografa il contenuto in busta.<br/>                                                                      |
| [**Crittografare**](envelopeddata-encrypt.md) | Crittografa il contenuto, crittografa una chiave di sessione per ogni destinatario e restituisce il BLOB crittografato.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **EnvelopedData** dispone di queste proprietà.



| Proprietà                                                  | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](envelopeddata-algorithm.md)<br/>   | Lettura/Scrittura<br/> | Algoritmo di crittografia e [*lunghezza della chiave*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Contenuto**](envelopeddata-content.md)<br/>       | Lettura/Scrittura<br/> | Contenuto di testo non crittografato di un messaggio da racchiudere. L'impostazione di questa proprietà deve essere eseguita prima che venga chiamato il metodo [**Encrypt**](envelopeddata-encrypt.md) .<br/> Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e qualsiasi contenuto crittografato nell'oggetto viene perso.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Destinatari**](envelopeddata-recipients.md)<br/> | Sola lettura<br/>  | Raccolta di oggetti [**certificato**](certificate.md) per ricevere il messaggio in busta digitale.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **EnvelopedData** ed è sicuro per lo scripting. Il ProgID per l'oggetto **EnvelopedData** è capicom. EnvelopedData. 1.

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
</dt> </dl>

 

 
