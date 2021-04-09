---
description: L'interfaccia IWiaItem2 fornisce applicazioni con le stesse funzionalità dell'interfaccia IWiaItem (la possibilità di eseguire query sui dispositivi per individuarne le funzionalità, per accedere alle interfacce di trasferimento dei dati e alle proprietà degli elementi e per controllare il dispositivo).
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: Interfaccia IWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879322"
---
# <a name="iwiaitem2-interface"></a>Interfaccia IWiaItem2

L'interfaccia **IWiaItem2** fornisce applicazioni con le stesse funzionalità dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la possibilità di eseguire query sui dispositivi per individuarne le funzionalità, per accedere alle interfacce di trasferimento dei dati e alle proprietà degli elementi e per controllare il dispositivo). Inoltre, fornisce all'applicazione la possibilità di creare e utilizzare in modo dinamico i filtri di elaborazione delle immagini che possono essere come estensioni dei driver di dispositivo Windows Image Acquisition (WIA) 2,0 disponibili in Windows Vista.

## <a name="members"></a>Membri

L'interfaccia **IWiaItem2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaItem2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaItem2** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckExtension**](-wia-iwiaitem2-checkextension.md)                 | Verifica se un'estensione specificata è disponibile nel computer e può essere usata dal metodo [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) . <br/>                                   |
| [**CreateChildItem**](-wia-iwiaitem2-createchilditem.md)               | Crea un nuovo elemento figlio. Aggiunge oggetti **IWiaItem2** all'albero **IWiaItem2** di un dispositivo. <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | Rimuove l'oggetto **IWiaItem2** corrente dalla struttura ad albero di oggetti del dispositivo. <br/>                                                                                                                          |
| [**DeviceCommand**](-wia-iwiaitem2-devicecommand.md)                   | Invia un comando a un dispositivo hardware WIA 2,0. <br/>                                                                                                                                                   |
| [**DeviceDlg**](-wia-iwiaitem2-devicedlg.md)                           | Visualizza una finestra di dialogo per preparare l'acquisizione dell'immagine. <br/>                                                                                                                              |
| [**Diagnostic**](-wia-iwiaitem2-diagnostic.md)                         | Non è attualmente supportato.<br/>                                                                                                                                                                          |
| [**EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)                 | Crea un oggetto enumeratore e passa di nuovo un puntatore alla relativa interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) per le cartelle con elementi nell'albero **IWiaItem2** di un dispositivo WIA 2,0. <br/>        |
| [**EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) | Crea un enumeratore usato per verificare i comandi e gli eventi supportati da un dispositivo WIA 2,0. <br/>                                                                                               |
| [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | Il metodo [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) crea un enumeratore usato per ottenere informazioni sugli eventi per i quali è stata registrata un'applicazione.<br/> |
| [**FindItemByName**](-wia-iwiaitem2-finditembyname.md)                 | Cerca nell'albero degli elementi secondari di un elemento usando il nome come chiave di ricerca. <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | Ottiene le interfacce di estensione che possono essere dotate di un driver di dispositivo WIA 2,0. <br/>                                                                                                                      |
| [**GetItemCategory**](-wia-iwiaitem2-getitemcategory.md)               | Ottiene le informazioni sulla categoria di un elemento. <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | Ottiene le informazioni sul tipo di un elemento. <br/>                                                                                                                                                                 |
| [**GetParentItem**](-wia-iwiaitem2-getparentitem.md)                   | Ottiene l'elemento padre nell'albero che rappresenta un dispositivo hardware WIA 2,0. <br/>                                                                                                                      |
| [**GetPreviewComponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | Ottiene il componente WIA 2,0 Preview.<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | Ottiene l'elemento radice di un albero di oggetti elemento utilizzato per rappresentare un dispositivo hardware WIA 2,0. <br/>                                                                                                        |



 

## <a name="remarks"></a>Commenti

L'albero degli elementi WIA 2,0 che un'applicazione può visualizzare è separato dall'albero che viene creato e gestito da un WIA 2,0 minidriver. Quando un minidriver crea un albero di elementi, il servizio WIA 2,0 utilizza questo albero degli elementi WIA 2,0 come guida per creare copie identiche che possono essere visualizzate dalle applicazioni di imaging. Gli elementi dell'albero copiato sono detti elementi dell'applicazione. Gli elementi dell'albero creati da un minidriver sono denominati elementi del driver. In Windows Vista gli alberi degli elementi WIA 2,0 sono compilati di oggetti **IWiaItem2** , ognuno dei quali implementa l'interfaccia **IWiaItem2** .

L'interfaccia **IWiaItem2** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
