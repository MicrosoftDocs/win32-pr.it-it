---
title: Elaborazione degli ambiti e manipolazione degli attributi
description: L'elaborazione dell'area di autenticazione, nota anche come manipolazione degli attributi, fa riferimento a trasformare il nome dell'utente che richiede l'accesso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728567"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Elaborazione degli ambiti e manipolazione degli attributi

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'elaborazione dell'area di autenticazione, nota anche come manipolazione degli attributi, fa riferimento a trasformare il nome dell'utente che richiede l'accesso. È anche possibile modificare l'ID della stazione chiamante e l'ID della stazione chiamata. Le regole di elaborazione dell'area di autenticazione fanno parte della raccolta di attributi del profilo proxy.

Per ogni manipolazione è necessario creare due attributi della [regola di manipolazione](/windows/desktop/Nps/sdo-manipulation-rule) . Ognuno di questi attributi è un valore stringa. La prima regola contiene un'espressione regolare che rappresenta il criterio di corrispondenza. La seconda regola contiene un'espressione regolare che rappresenta il testo di sostituzione. È anche necessario creare un attributo di [destinazione della manipolazione](/windows/desktop/Nps/sdo-manipulation-target) . Questo attributo è un'enumerazione che specifica la parte delle informazioni dell'utente da modificare.

L'ordine in cui vengono creati gli attributi è importante. NPS elabora gli attributi nell'ordine in cui sono stati creati.

Nella tabella seguente viene illustrato un esempio di un set di attributi di manipolazione.



| Nome                 | Tipo         | Valore stringa     |
|----------------------|--------------|------------------|
| msManipulationRule   | **\_BSTR VT** | "@company.com"   |
| msManipulationRule   | **\_BSTR VT** | "@microsoft.com" |
| msManipulationRule   | **\_BSTR VT** | "^.+@"           |
| msManipulationRule   | **\_BSTR VT** | "guest@"         |
| msManipulationTarget | **VT \_ I4**   | "1"              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gerarchia del modello a oggetti](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Attributi supportati da SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Creazione di un criterio di richiesta di connessione](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 