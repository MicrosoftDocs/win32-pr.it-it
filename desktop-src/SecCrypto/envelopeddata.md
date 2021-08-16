---
description: L'oggetto EnvelopedData fornisce proprietà e metodi per avvolgono i dati per la privacy tramite crittografia.
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
ms.openlocfilehash: af88fd9b4be0c7ddd9fe5dfc204558c1a36cab418166f73c8de0ec0c06c0a8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766112"
---
# <a name="envelopeddata-object"></a>Oggetto EnvelopedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto EnvelopedData** fornisce proprietà e metodi per avvolgono i dati per la privacy tramite crittografia. Per invidiare i dati, viene generata una chiave crittografica di sessione. Tale [*chiave di sessione*](../secgloss/s-gly.md) viene quindi crittografata per ogni destinatario previsto usando la chiave pubblica del destinatario previsto dal certificato del destinatario. [](../secgloss/p-gly.md) I dati crittografati e il set di chiavi di sessione crittografate possono essere inviati a tutti i destinatari previsti. Il messaggio generato è in formato PKCS \# 7.

## <a name="members"></a>Membri

**L'oggetto EnvelopedData** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto EnvelopedData** dispone di questi metodi.



| Metodo                                   | Descrizione                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Decrittografare**](envelopeddata-decrypt.md) | Decrittografa il contenuto in busta.<br/>                                                                      |
| [**Crittografare**](envelopeddata-encrypt.md) | Crittografa il contenuto, crittografa una chiave di sessione per ogni destinatario e restituisce il BLOB crittografato.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto EnvelopedData** ha queste proprietà.



| Proprietà                                                  | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](envelopeddata-algorithm.md)<br/>   | Lettura/Scrittura<br/> | Algoritmo di crittografia e [*lunghezza della chiave*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Contenuto**](envelopeddata-content.md)<br/>       | Lettura/Scrittura<br/> | Contenuto di testo non crittografato di un messaggio da inviare in busta. L'impostazione di questa proprietà deve essere eseguita prima [**della chiamata del**](envelopeddata-encrypt.md) metodo Encrypt.<br/> Quando il valore di questa proprietà viene reimpostato, [](../secgloss/s-gly.md) direttamente o indirettamente, l'intero stato dell'oggetto viene reimpostato e qualsiasi contenuto crittografato nell'oggetto viene perso.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Destinatari**](envelopeddata-recipients.md)<br/> | Sola lettura<br/>  | Raccolta di [**oggetti Certificate**](certificate.md) per ricevere il messaggio in busta.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Commenti

**L'oggetto EnvelopedData** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto EnvelopedData** è CAPICOM. EnvelopedData.1.

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
</dt> </dl>

 

 
