---
title: Interfaccia IWMDRMProvider
description: L'interfaccia IWMDRMProvider fornisce un metodo per la creazione degli altri oggetti delle API estese del client DRM di Microsoft Windows Media. è possibile ottenere un puntatore a un'istanza di questa interfaccia chiamando la funzione WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Formato Windows Media Interface IWMDRMProvider
- Interfaccia IWMDRMProvider-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729215"
---
# <a name="iwmdrmprovider-interface"></a>Interfaccia IWMDRMProvider

L'interfaccia **IWMDRMProvider** fornisce un metodo per la creazione degli altri oggetti delle API estese del client DRM di Microsoft Windows Media.

È possibile ottenere un puntatore a un'istanza di questa interfaccia chiamando la funzione [**WMDRMCreateProvider**](wmdrmcreateprovider.md) . Per ottenere un puntatore a un'istanza di questa interfaccia in grado di creare oggetti protetti, è necessario chiamare la funzione [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMProvider** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMProvider** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMProvider** dispone di questi metodi.



| Metodo                                              | Descrizione                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**CreateObject**](iwmdrmprovider-createobject.md) | Recupera un puntatore a un'interfaccia specificata, creando l'oggetto di implementazione, se necessario.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

