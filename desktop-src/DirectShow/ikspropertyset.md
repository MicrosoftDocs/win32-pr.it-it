---
description: L'interfaccia IKsPropertySet è stata originariamente progettata come un modo efficiente per impostare e recuperare le proprietà dei dispositivi nei driver WDM, usando KSProxy per tradurre le chiamate al metodo COM in modalità utente nei set di proprietà in modalità kernel usati dai driver della classe di streaming WDM. Questa interfaccia viene ora utilizzata anche per passare le informazioni esclusivamente tra i componenti software. In alcuni casi, i componenti software devono implementare questa interfaccia, altrimenti l'interfaccia IKsControl (documentata in DirectShow DDK). Se, ad esempio, si scrive un decodificatore MPEG-2 software da utilizzare con lo strumento di spostamento DVD, è necessario implementare una di queste interfacce e supportare anche i set di proprietà correlati a DVD che lo strumento di spostamento invierà al decodificatore. I pin possono supportare una di queste interfacce per consentire ad altri pin o filtri di impostare o recuperare le proprietà. Si noti che nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome. Le due interfacce non sono compatibili. L'interfaccia IKsControl, documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interfaccia IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480772"
---
# <a name="ikspropertyset-interface"></a>Interfaccia IKsPropertySet

L' `IKsPropertySet` interfaccia è stata originariamente progettata come un modo efficiente per impostare e recuperare le proprietà dei dispositivi nei driver WDM, usando ksproxy per tradurre le chiamate al metodo com in modalità utente nei set di proprietà in modalità kernel usati dai driver della classe di streaming WDM. Questa interfaccia viene ora utilizzata anche per passare le informazioni esclusivamente tra i componenti software.

In alcuni casi, i componenti software devono implementare questa interfaccia, altrimenti l'interfaccia **IKsControl** (documentata in DirectShow DDK). Se, ad esempio, si scrive un decodificatore MPEG-2 software da utilizzare con lo [strumento di spostamento DVD](dvd-navigator-filter.md), è necessario implementare una di queste interfacce e supportare anche i set di proprietà correlati a DVD che lo strumento di spostamento invierà al decodificatore. I pin possono supportare una di queste interfacce per consentire ad altri pin o filtri di impostare o recuperare le proprietà.

> [!Note]  
> Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome. Le due interfacce non sono compatibili. L'interfaccia **IKsControl** , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.

 

## <a name="members"></a>Membri

L'interfaccia **IKsPropertySet** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPropertySet** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IKsPropertySet** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Ottieni**](ikspropertyset-get.md)                       | Recupera una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.<br/> |
| [**QuerySupported**](ikspropertyset-querysupported.md) | Determina se un oggetto supporta un set di proprietà specificato.<br/>           |
| [**Set**](ikspropertyset-set.md)                       | Imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.<br/>      |



 

## <a name="remarks"></a>Commenti

Prima di ksproxy. h, è necessario includere KS. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Libreria<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 
