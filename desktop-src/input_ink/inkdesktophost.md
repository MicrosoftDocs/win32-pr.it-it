---
description: Implementa l'interfaccia IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Classe InkDesktopHost
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689224"
---
# <a name="inkdesktophost-class"></a>Classe InkDesktopHost

Implementa [**l'interfaccia IInkDesktopHost.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)

Un oggetto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) consente l'input penna, l'elaborazione e il rendering tramite la creazione di un thread dell'app per ospitare un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inserirlo nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.

## <a name="members"></a>Membri

La **classe InkDesktopHost** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkDesktopHost** include anche questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe InkDesktopHost** include questi metodi.

| Metodo | Descrizione |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Crea un [**oggetto IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in un thread dell'applicazione, lo connette alla struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app e imposta le dimensioni dell'oggetto.<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Crea un [**oggetto IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in un thread dell'applicazione.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Aggiungere un'operazione di input penna a una coda di lavoro per l'esecuzione nel thread **InkDesktopHost.**<br/> |

## <a name="creationaccess-functions"></a>Creazione di \\ funzioni di accesso

Chiamare [<strong>CoCreateInstance con</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) l'identificatore di <strong>classe InkDesktopHost</strong> per recuperare un riferimento all'oggetto.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|---|---|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/> |
| Intestazione<br/>                   | <dl> <dt>InkPresenterDesktop.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>InkPresenterDesktop.idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost è definito come 4ce7d875-a981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Classi del presentatore di input](ink-presenter-classes.md)penna, interazioni con penna e [stilo,](/windows/uwp/design/input/pen-and-stylus-interactions) [esempio di](/samples/microsoft/windows-universal-samples/inkanalysis/)analisi dell'input penna, esempio di input [penna semplice,](/samples/microsoft/windows-universal-samples/simpleink/)esempio di input penna [complesso](/samples/microsoft/windows-universal-samples/complexink/)
