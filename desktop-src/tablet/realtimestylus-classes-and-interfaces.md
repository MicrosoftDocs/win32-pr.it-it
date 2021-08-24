---
description: Questa sezione contiene informazioni sulle interfacce e le classi usate nello stilo in tempo reale.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Classi e interfacce RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd842219a23accc076ff7fdc8564ccb3ce0c472cb7e26ab036f1048456461f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589951"
---
# <a name="realtimestylus-classes-and-interfaces"></a>Classi e interfacce RealTimeStylus

Questa sezione contiene informazioni sulle interfacce e le classi usate nello stilo in tempo reale.

> [!Note]  
> Le classi e le interfacce dello stilo in tempo reale non sono conformi ad Automazione.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Classe                                                      | Descrizione                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Classe RealTimeStylus**](realtimestylus-class.md)       | Implementa [**l'interfaccia IRealTimeStylus.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)<br/>                 |
| [**Classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementa [**l'interfaccia IDynamicRenderer.**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)<br/>     |
| [**Classe GestureRecognizer**](gesturerecognizer-class.md) | Implementa [**l'interfaccia IGestureRecognizer.**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)<br/> |
| [**Classe StrokeBuilder**](strokebuilder-class.md)         | Implementa [**l'interfaccia IStrokeBuilder.**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)<br/>         |



 

## <a name="interfaces"></a>Interfacce



| Interfaccia                                                                          | Descrizione                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Espone metodi che consentono di controllare la visualizzazione dei dati dello stilo in tempo reale quando i dati vengono gestiti [**dall'oggetto Classe RealTimeStylus.**](realtimestylus-class.md)<br/> |
| [**Interfaccia IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Espone metodi che consentono di reagire agli eventi riconoscendo i movimenti dello stilo e consentendo di aggiungere dati alla coda di input.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Gestisce i dati dei pacchetti dello stilo da un digitalizzatore in tempo reale.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Estende l'interfaccia IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Estende l'interfaccia IRealTimeStylus.<br/>                                                                                                                                           |
| [**Interfaccia IRealTimeStylusSynchronization**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Sincronizza l'accesso [**all'oggetto classe RealTimeStylus.**](realtimestylus-class.md)<br/>                                                                                          |
| [**Interfaccia IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Espone metodi che consentono di creare tratti a livello di codice.<br/>                                                                                                              |
| [**Interfaccia IStylusPlugin**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Espone metodi che consentono di ricevere notifiche di eventi ed eseguire l'elaborazione personalizzata in base a tali eventi.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Rappresenta un plug-in asincrono che può essere aggiunto alla raccolta di plug-in asincroni della classe [**RealTimeStylus.**](realtimestylus-class.md)<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Rappresenta un plug-in sincrono che può essere aggiunto alla raccolta di plug-in sincroni della classe [**RealTimeStylus.**](realtimestylus-class.md)<br/>                                   |



 

## <a name="return-values"></a>Valori restituiti

I metodi nella libreria COM restituiscono valori **di HRESULT.** Se non specificato diversamente, i significati dei **valori HRESULT** sono descritti nella tabella seguente.



| Valore HRESULT                                   | Descrizione                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Operazione completata.<br/>                                                                      |
| PUNTATORE \_ E<br/>                           | Almeno un puntatore (per un parametro di input o di output) non è valido.<br/> |
| E \_ INVALIDARG<br/>                        | Il membro ha tentato di passare un argomento non valido.<br/>                              |
| ECCEZIONE \_ INPUT \_ PENNA E<br/>                    | Si è verificata un'eccezione.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | Impossibile allocare memoria per completare l'operazione.<br/>                      |
| E \_ FAIL<br/>                              | Si è verificato un errore non specificato.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Il membro ha tentato di usare un'operazione non valida.<br/>                                 |
| MODALITÀ TPC \_ E \_ NON \_ VALIDA<br/>                | Il membro ha tentato di usare una modalità non valida.<br/>                                      |
| CONFIGURAZIONE TPC \_ E \_ NON \_ VALIDA<br/>       | Il membro ha tentato di usare una configurazione non valida.<br/>                             |
| DESCRIZIONE \_ DEL PACCHETTO TPC E NON \_ \_ \_ VALIDA<br/> | Il membro ha tentato di usare una descrizione del pacchetto non valida.<br/>                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su RealTimeStylus](realtimestylus-reference.md)
</dt> </dl>

 

 
