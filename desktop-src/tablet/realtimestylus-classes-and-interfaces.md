---
description: Questa sezione contiene informazioni sulle interfacce e sulle classi usate nello stilo in tempo reale.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Classi e interfacce RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882777"
---
# <a name="realtimestylus-classes-and-interfaces"></a>Classi e interfacce RealTimeStylus

Questa sezione contiene informazioni sulle interfacce e sulle classi usate nello stilo in tempo reale.

> [!Note]  
> Le interfacce e le classi stilo in tempo reale non sono conformi all'automazione.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Classe                                                      | Descrizione                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Classe RealTimeStylus**](realtimestylus-class.md)       | Implementa l'interfaccia [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .<br/>                 |
| [**Classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementa l'interfaccia dell' [**interfaccia IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .<br/>     |
| [**Classe GestureRecognizer**](gesturerecognizer-class.md) | Implementa l'interfaccia dell' [**interfaccia IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .<br/> |
| [**Classe StrokeBuilder**](strokebuilder-class.md)         | Implementa l'interfaccia dell' [**interfaccia IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .<br/>         |



 

## <a name="interfaces"></a>Interfacce



| Interfaccia                                                                          | Descrizione                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Espone metodi che consentono di controllare la visualizzazione dei dati dello stilo in tempo reale poiché i dati vengono gestiti dall'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) .<br/> |
| [**Interfaccia IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Espone metodi che consentono di reagire agli eventi riconoscendo i movimenti dello stilo e consentendo di aggiungere dati alla coda di input.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Gestisce i dati del pacchetto dello stilo da un digitalizzatore in tempo reale.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Estende l'interfaccia IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Estende l'interfaccia IRealTimeStylus.<br/>                                                                                                                                           |
| [**Interfaccia IRealTimeStylusSynchronization**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Sincronizza l'accesso all'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                                                                          |
| [**Interfaccia IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Espone metodi che consentono di creare tratti a livello di codice.<br/>                                                                                                              |
| [**Interfaccia IStylusPlugin**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Espone metodi che consentono di ricevere notifiche di eventi e di eseguire l'elaborazione personalizzata in base a tali eventi.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Rappresenta un plug-in asincrono che può essere aggiunto alla raccolta di plug-in asincrona della [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Rappresenta un plug-in sincrono che può essere aggiunto alla raccolta di plug-in sincrona della [**classe RealTimeStylus**](realtimestylus-class.md) .<br/>                                   |



 

## <a name="return-values"></a>Valori restituiti

I metodi nella libreria COM restituiscono valori **HRESULT**. Se non specificato diversamente, i significati dei valori **HRESULT** sono descritti nella tabella seguente.



| Valore HRESULT                                   | Descrizione                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| \_OK<br/>                                | Esito positivo.<br/>                                                                      |
| \_puntatore E<br/>                           | Almeno un puntatore (per un parametro di input o di output) non è valido.<br/> |
| E \_ INVALIDARG<br/>                        | Il membro ha tentato di passare un argomento non valido.<br/>                              |
| E \_ \_ eccezione Ink<br/>                    | Si è verificata un'eccezione.<br/>                                                           |
| E \_ OutOfMemory<br/>                       | Il sistema non è in grado di allocare memoria per completare l'operazione.<br/>                      |
| E \_ non riescono<br/>                              | Si è verificato un errore non specificato.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Il membro ha tentato di usare un'operazione non valida.<br/>                                 |
| \_modalità TPC E \_ non valida \_<br/>                | Il membro ha tentato di usare una modalità non valida.<br/>                                      |
| \_configurazione TPC E \_ non valida \_<br/>       | Il membro ha tentato di usare una configurazione non valida.<br/>                             |
| \_Descrizione pacchetto TPC E \_ non valida \_ \_<br/> | Il membro ha tentato di usare una descrizione del pacchetto non valida.<br/>                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a RealTimeStylus](realtimestylus-reference.md)
</dt> </dl>

 

 
