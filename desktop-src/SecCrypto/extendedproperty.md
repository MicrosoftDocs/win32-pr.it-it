---
description: Rappresenta una proprietà estesa a Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329224"
---
# <a name="extendedproperty-object"></a>ExtendedProperty (oggetto)

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

L'oggetto **ExtendedProperty** rappresenta una proprietà estesa da Microsoft.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **ExtendedProperty** viene utilizzato per eseguire le attività seguenti:

-   Imposta o Recupera il tipo della proprietà estesa.
-   Imposta o Recupera il tipo di codifica utilizzato per codificare la proprietà estesa.

## <a name="members"></a>Membri

L'oggetto **ExtendedProperty** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ExtendedProperty** dispone di queste proprietà.



| Proprietà                                             | Tipo di accesso           | Descrizione                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Lettura/Scrittura<br/> | Valore dell'enumerazione [**\_ propid di CAPICOM**](capicom-propid.md) che imposta o Recupera il tipo di proprietà estesa.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Valore**](extendedproperty-value.md)<br/>   | Lettura/Scrittura<br/> | Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che imposta o recupera i dati della proprietà estesa.<br/>                              |



 

## <a name="remarks"></a>Commenti

L'oggetto **ExtendedProperty** viene usato dalla raccolta [**ExtendedProperties**](extendedproperties.md) .

È possibile creare l'oggetto **ExtendedProperty** e non è sicuro per lo scripting. Il ProgID per l'oggetto **ExtendedProperty** è capicom. ExtendedProperty. 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
