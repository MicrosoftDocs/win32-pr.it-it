---
description: Rappresenta una proprietà estesa da Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Oggetto ExtendedProperty
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
ms.openlocfilehash: 927d35f73cec1f9e9032c326097a642349d6faa7e02d533330303016184a4bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007049"
---
# <a name="extendedproperty-object"></a>Oggetto ExtendedProperty

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

**L'oggetto ExtendedProperty** rappresenta una proprietà estesa da Microsoft.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto ExtendedProperty** viene usato per eseguire le attività seguenti:

-   Imposta o recupera il tipo della proprietà estesa.
-   Imposta o recupera il tipo di codifica usato per codificare la proprietà estesa.

## <a name="members"></a>Membri

**L'oggetto ExtendedProperty** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ExtendedProperty** ha queste proprietà.



| Proprietà                                             | Tipo di accesso           | Descrizione                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Lettura/Scrittura<br/> | Valore [**dell'enumerazione CAPICOM \_ PROPID**](capicom-propid.md) che imposta o recupera il tipo di proprietà estesa.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Valore**](extendedproperty-value.md)<br/>   | Lettura/Scrittura<br/> | Valore dell'enumerazione [**CAPICOM \_ ENCODING \_ TYPE**](capicom-encoding-type.md) che imposta o recupera i dati delle proprietà estese.<br/>                              |



 

## <a name="remarks"></a>Commenti

**L'oggetto ExtendedProperty** viene usato dalla [**raccolta ExtendedProperties.**](extendedproperties.md)

**L'oggetto ExtendedProperty** può essere creato e non è sicuro per lo scripting. Il ProgID per **l'oggetto ExtendedProperty** è CAPICOM. ExtendedProperty.1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
