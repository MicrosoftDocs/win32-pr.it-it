---
description: Interfaccia implementata dal client che consente agli sviluppatori di fornire le proprie credenziali in modo dinamico in fase di esecuzione per autenticare i contenitori non aggiunti a un dominio con Active Directory.
title: Interfaccia ICcgDomainAuthCredentials (ccgplugins.h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387833"
---
# <a name="iccgdomainauthcredentials-interface"></a>Interfaccia ICcgDomainAuthCredentials

Interfaccia implementata dal client che consente agli sviluppatori di fornire le proprie credenziali in modo dinamico in fase di esecuzione per autenticare i contenitori non aggiunti a un dominio con Active Directory. 

## <a name="members"></a>Membri

**L'interfaccia ICcgDomainAuthCredentials** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ICcgDomainAuthCredentials** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ICcgDomainAuthCredentials** include questi metodi.



| Metodo                                           | Descrizione                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetPasswordCredentials**](iccgdomainauthcredentials-getpasswordcredentials.md)               | Restituisce le credenziali per autenticare un contenitore non aggiunto a un dominio con Active Directory.<br/>                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ccgplugins.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>ccgplugins.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

