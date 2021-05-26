---
description: Mostra i membri della classe CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Membri CXAPOParametersBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554aa66b4166bc3d0de4db685e0f6e7b54e6ebf5
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423871"
---
# <a name="cxapoparametersbase-members"></a>Membri CXAPOParametersBase

Mostra i membri della [**classe CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)

## <a name="public-constructors"></a>Costruttori pubblici



|    Costruttore                                                |     Descrizione                                                                    |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Costruisce un [**oggetto CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) |



 

## <a name="public-methods"></a>Metodi pubblici



|        Metodo                                                                                                                      |     Descrizione                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                         | Incrementa il conteggio dei riferimenti dell'oggetto XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Restituisce i parametri del processo corrente. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                           | Restituisce il numero di frame di input necessari per generare il numero specificato di frame di output.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Restituisce il numero di frame di output necessari per generare il numero specificato di frame di input.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifica a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) che XAPO ha terminato l'accesso ai parametri del processo corrente. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (ereditato da [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Ottiene parametri specifici dell'effetto. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Restituisce le proprietà di registrazione di un oggetto XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                     | Esegue qualsiasi inizializzazione specifica dell'effetto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)             | Esegue una query se un formato di input specifico è supportato per un formato di output specificato.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)           | Esegue una query se un formato di output specifico è supportato per un formato di input specificato.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                             | Notifica a XAPO i formati di flusso che [**verranno**](/windows/win32/api/xapo/nf-xapo-ixapo-process) trasmessi al processo.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Chiamato da [**IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) per consentire la convalida dei parametri definiti dall'utente. <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indica se [**IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) è stato chiamato dall'ultimo passaggio di elaborazione. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Recupera il puntatore a interfaccia richiesto se il XAPO lo supporta.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                       | Decrementa il conteggio dei riferimenti dell'oggetto XAPO ed elimina l'oggetto se il conteggio dei riferimenti scende a zero.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                               | Restituisce l'oggetto allo stato in cui si è presente subito dopo [**la chiamata a LockForProcess.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (ereditato da [**IXAPOParameters)**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) | Imposta parametri specifici dell'effetto.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (ereditato da [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Opposto a LockForProcess: le variabili allocate durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devono essere deallocate in questo metodo.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
