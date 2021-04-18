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
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320436"
---
# <a name="inkdesktophost-class"></a>Classe InkDesktopHost

Implementa l'interfaccia [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .

Un oggetto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) consente l'input, l'elaborazione e il rendering dell'input penna tramite la creazione di un thread dell'applicazione per ospitare un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inserirlo nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.

## <a name="members"></a>Membri

La classe **InkDesktopHost** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkDesktopHost** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **InkDesktopHost** dispone di questi metodi.

| Metodo | Descrizione |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Crea un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in un thread dell'applicazione, lo connette alla struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app e imposta le dimensioni dell'oggetto.<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Crea un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in un thread dell'applicazione.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Aggiungere un'operazione Ink a una coda di lavoro per l'esecuzione nel thread **InkDesktopHost** .<br/> |

## <a name="creationaccess-functions"></a>Funzioni di accesso per la creazione \\

Chiamare [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe <strong>InkDesktopHost</strong> per recuperare un riferimento all'oggetto.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|---|---|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/> |
| Intestazione<br/>                   | <dl> <dt>InkPresenterDesktop. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>InkPresenterDesktop. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost è definito come 4ce7d875-a981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Classi Presenter di input](ink-presenter-classes.md)penna, [interazioni di penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)
