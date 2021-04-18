---
description: Mostra i membri della classe CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Membri di CXAPOParametersBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e225d1628408b5d5472bed8c3060f714bb7b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314422"
---
# <a name="cxapoparametersbase-members"></a>Membri di CXAPOParametersBase

Mostra i membri della classe [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

## <a name="public-constructors"></a>Costruttori pubblici



|                                                    |                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Costruisce un oggetto [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) . |



 

## <a name="public-methods"></a>Metodi pubblici



|                                                                                                                              |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Incrementa il conteggio dei riferimenti dell'oggetto XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Restituisce i parametri del processo corrente. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                           | Restituisce il numero di fotogrammi di input necessari per generare il numero specificato di fotogrammi di output.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Restituisce il numero di frame di output necessari per generare il numero specificato di fotogrammi di input.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifica a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) che il XAPO ha completato l'accesso ai parametri del processo corrente. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (Ereditato da [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Ottiene i parametri specifici dell'effetto. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Restituisce le proprietà di registrazione di un XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                     | Esegue qualsiasi inizializzazione specifica dell'effetto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))             | Esegue una query se è supportato un formato di input specifico per un determinato formato di output.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))           | Esegue una query se è supportato un formato di output specifico per un determinato formato di input.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                             | Viene inviata una notifica a XAPO del [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) di formattazione dei flussi.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Chiamata eseguita da [**IXAPOParameters:: Separameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) per consentire la convalida dei parametri definiti dall'utente. <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indica se [**IXAPOParameters:: Separameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) è stato chiamato dopo l'ultimo passaggio di elaborazione. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Recupera il puntatore a interfaccia richiesto se XAPO lo supporta.<br/>                                                                                    |
| [**Versione**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (ereditata da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Decrementa il conteggio dei riferimenti dell'oggetto XAPO ed Elimina l'oggetto se il conteggio dei riferimenti scende a zero.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                               | Restituisce l'oggetto allo stato in cui si trovava subito dopo la chiamata a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**Parametri**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (ereditati da [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Imposta i parametri specifici dell'effetto.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Opposto a LockForProcess: le variabili allocate durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devono essere deallocate in questo metodo.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
