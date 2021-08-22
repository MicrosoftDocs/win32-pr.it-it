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
ms.openlocfilehash: 0225582217df56f486a44f12e3ca6ea0003130fdb209fb67e9f9e4ee258764d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007239"
---
# <a name="extendedproperties-object"></a>Oggetto ExtendedProperties

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

**L'oggetto ExtendedProperties** rappresenta una raccolta [**di oggetti ExtendedProperty.**](extendedproperty.md) Ogni oggetto rappresenta una singola proprietà estesa.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto ExtendedProperties** viene usato per eseguire le attività seguenti:

-   Aggiungere o rimuovere [**un oggetto ExtendedProperty**](extendedproperty.md) dalla raccolta.
-   Recupera il numero di proprietà estese nella raccolta.
-   Recuperare un [**oggetto ExtendedProperty**](extendedproperty.md) specifico dalla raccolta.
-   Scorrere la raccolta.

## <a name="members"></a>Membri

**L'oggetto ExtendedProperties** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#extendedproperties-object)

### <a name="methods"></a>Metodi

**L'oggetto ExtendedProperties** dispone di questi metodi.



| Metodo                                      | Descrizione                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Aggiungere**](extendedproperties-add.md)       | Aggiunge un [**oggetto ExtendedProperty**](extendedproperty.md) alla raccolta.<br/>      |
| [**Rimuovi**](extendedproperties-remove.md) | Rimuove un [**oggetto ExtendedProperty**](extendedproperty.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto ExtendedProperties** ha queste proprietà.



| Proprietà                                                   | Tipo di accesso          | Descrizione                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Sola lettura<br/> | Recupera [**un'interfaccia IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta in Visual Basic Scripting Edition (VBScript).<br/> |
| [**Conteggio**](extendedproperties-count.md)<br/>       | Sola lettura<br/> | Recupera il numero di [**oggetti ExtendedProperty**](extendedproperty.md) nella raccolta.<br/>                                                                                                                      |
| [**Elemento**](extendedproperties-item.md)<br/>         | Sola lettura<br/> | Recupera un [**oggetto ExtendedProperty**](extendedproperty.md) che rappresenta la proprietà estesa indicizzata della raccolta. Questa è la proprietà predefinita.<br/>                                                      |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto ExtendedProperties.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
