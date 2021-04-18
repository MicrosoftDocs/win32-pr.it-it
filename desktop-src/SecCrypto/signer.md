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
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332008"
---
# <a name="signer-object"></a>Oggetto firmatario

\[L'oggetto **firmatario** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L'oggetto **firmatario** stabilisce il firmatario di un oggetto [**SignedData**](signeddata.md) o [**SignedCode**](signedcode.md) . Il [**certificato**](certificate.md) dell'oggetto **firmatario** deve avere una chiave privata disponibile che può essere usata per firmare i dati.

## <a name="members"></a>Membri

L'oggetto **firmatario** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **firmatario** presenta questi metodi.



| Metodo                      | Descrizione                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Caricamento**](signer-load.md) | Carica un certificato di firma da un file PFX specificato.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **firmatario** presenta queste proprietà.



| Proprietà                                                                     | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Sola lettura<br/>  | Raccolta di attributi autenticati.<br/>                                                                                                                                                                                                                                                                                      |
| [**Certificato**](signer-certificate.md)<br/>                         | Lettura/Scrittura<br/> | Oggetto [**certificato**](certificate.md) che rappresenta il certificato di un firmatario dei dati.<br/> Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Catena**](signer-chain.md)<br/>                                     | Sola lettura<br/>  | Catena del firmatario.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Opzioni**](signer-options.md)<br/>                                 | Lettura/Scrittura<br/> | Imposta o recupera l'opzione del certificato del firmatario.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **firmatario** ed è sicuro per lo scripting. Il ProgID per l'oggetto **firmatario** è capicom. Firmatario. 2.

**CAPICOM 1. *x*:** il ProgID per l'oggetto **firmatario** è capicom. Firmatario. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
