---
description: Mostra i membri della classe CXAPOBase.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Membri di CXAPOBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab63cf7e8ac6e4d0fa14ec412b53682aff2ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057837"
---
# <a name="cxapobase-members"></a>Membri di CXAPOBase

Mostra i membri della classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

## <a name="public-constructors"></a>Costruttori pubblici



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Costruisce un oggetto [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) . |



 

## <a name="public-methods"></a>Metodi pubblici



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                   | Incrementa il conteggio dei riferimenti dell'oggetto XAPO.<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                     | Restituisce il numero di fotogrammi di input necessari per generare il numero specificato di fotogrammi di output.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Restituisce il numero di frame di output necessari per generare il numero specificato di fotogrammi di input.<br/>                                                            |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) | Restituisce le proprietà di registrazione di un XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                               | Esegue qualsiasi inizializzazione specifica dell'effetto.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Esegue una query se è supportato un formato di input specifico per un determinato formato di output.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))     | Esegue una query se è supportato un formato di output specifico per un determinato formato di input.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                       | Viene inviata una notifica a XAPO del [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) di formattazione dei flussi.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Recupera il puntatore a interfaccia richiesto se XAPO lo supporta.<br/>                                                                                    |
| [**Versione**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (ereditata da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Decrementa il conteggio dei riferimenti dell'oggetto XAPO ed Elimina l'oggetto se il conteggio dei riferimenti scende a zero.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Restituisce l'oggetto allo stato in cui si trovava subito dopo la chiamata a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (Ereditato da [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Opposto a LockForProcess: le variabili allocate durante [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) devono essere deallocate in questo metodo.<br/> |



 

## <a name="protected-methods"></a>Metodi protetti



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Restituisce un puntatore alla struttura [**delle \_ \_ proprietà di registrazione XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)che contiene le proprietà di registrazione con cui è stato creato il XAPO.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Verifica se il XAPO è bloccato.<br/>                                                                                                                                                |
| LONG m \_ lReferenceCount<br/>                                                       | Conteggio dei riferimenti COM dell'oggetto XAPO.<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Chiamata eseguita da un'implementazione [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) quando un XAPO è disabilitato per l'elaborazione tramite.<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Verifica che un formato audio rientri negli intervalli predefiniti supportati.<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Verifica che la configurazione di una coppia di formato di input e output sia supportata rispetto ai flag di proprietà XAPO.<br/>                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
