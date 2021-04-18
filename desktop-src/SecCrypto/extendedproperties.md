---
description: Rappresenta una raccolta di oggetti ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Oggetto ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329226"
---
# <a name="extendedproperties-object"></a>Oggetto ExtendedProperties

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

L'oggetto **ExtendedProperties** rappresenta una raccolta di oggetti [**ExtendedProperty**](extendedproperty.md) . Ogni oggetto rappresenta una singola proprietà estesa.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **ExtendedProperties** viene utilizzato per eseguire le attività seguenti:

-   Aggiungere o rimuovere un oggetto [**ExtendedProperty**](extendedproperty.md) dalla raccolta.
-   Recuperare il numero di proprietà estese nella raccolta.
-   Recuperare un oggetto [**ExtendedProperty**](extendedproperty.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

L'oggetto **ExtendedProperties** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#extendedproperties-object)

### <a name="methods"></a>Metodi

L'oggetto **ExtendedProperties** dispone di questi metodi.



| Metodo                                      | Descrizione                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Aggiungere**](extendedproperties-add.md)       | Aggiunge un oggetto [**ExtendedProperty**](extendedproperty.md) alla raccolta.<br/>      |
| [**Rimuovi**](extendedproperties-remove.md) | Rimuove un oggetto [**ExtendedProperty**](extendedproperty.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **ExtendedProperties** dispone di queste proprietà.



| Proprietà                                                   | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Sola lettura<br/> | Recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](extendedproperties-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di oggetti [**ExtendedProperty**](extendedproperty.md) nell'insieme.<br/>                                                                                                                      |
| [**Elemento**](extendedproperties-item.md)<br/>         | Sola lettura<br/> | Recupera un oggetto [**ExtendedProperty**](extendedproperty.md) che rappresenta la proprietà estesa indicizzata della raccolta. Si tratta della proprietà predefinita.<br/>                                                      |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **ExtendedProperty** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
