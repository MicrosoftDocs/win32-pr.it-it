---
description: Stabilisce il firmatario di un oggetto SignedData o SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Oggetto firmatario
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4da0f63c64a85290d5b36cad046446a9a0feedcd897869a0df1932ee2532a687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898513"
---
# <a name="signer-object"></a>Oggetto firmatario

\[**L'oggetto** Firmatario è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**L'oggetto Signer** stabilisce il firmatario di un [**oggetto SignedData**](signeddata.md) [**o SignedCode.**](signedcode.md) Il [**certificato**](certificate.md) **dell'oggetto Firmatario** deve avere una chiave privata disponibile che può essere usata per firmare i dati.

## <a name="members"></a>Membri

**L'oggetto Firmatario** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Firmatario** dispone di questi metodi.



| Metodo                      | Descrizione                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Caricamento**](signer-load.md) | Carica un certificato di firma da un file PFX specificato.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto Firmatario** ha queste proprietà.



| Proprietà                                                                     | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Sola lettura<br/>  | Raccolta di attributi autenticati.<br/>                                                                                                                                                                                                                                                                                      |
| [**Certificato**](signer-certificate.md)<br/>                         | Lettura/Scrittura<br/> | Oggetto [**Certificate**](certificate.md) che rappresenta il certificato di un firmatario dei dati.<br/> Quando il valore di questa proprietà viene reimpostato, [](../secgloss/s-gly.md) direttamente o indirettamente, viene reimpostato l'intero stato dell'oggetto.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Catena**](signer-chain.md)<br/>                                     | Sola lettura<br/>  | Catena del firmatario.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Opzioni**](signer-options.md)<br/>                                 | Lettura/Scrittura<br/> | Imposta o recupera l'opzione del certificato del firmatario.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

**L'oggetto Firmatario** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto Signer** è CAPICOM. Firmatario.2.

**CAPICOM 1. *x*:** ProgID per l'oggetto **Signer** è CAPICOM. Firmatario.1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
