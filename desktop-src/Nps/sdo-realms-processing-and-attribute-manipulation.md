---
title: Elaborazione delle aree di autenticazione e manipolazione degli attributi
description: L'elaborazione delle aree di autenticazione, nota anche come manipolazione degli attributi, si riferisce alla trasformazione del nome dell'utente che richiede l'accesso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8054ad8234ca4772a52619d83bc85a9d357f2cf8da2f1c969eed918c75a8305a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618947"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Elaborazione delle aree di autenticazione e manipolazione degli attributi

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'elaborazione delle aree di autenticazione, nota anche come manipolazione degli attributi, si riferisce alla trasformazione del nome dell'utente che richiede l'accesso. È anche possibile modificare l'ID stazione chiamante e l'ID stazione chiamata. Le regole di elaborazione delle aree di autenticazione fanno parte della raccolta di attributi del profilo proxy.

Per ogni manipolazione, è necessario creare due [attributi manipulation-rule.](/windows/desktop/Nps/sdo-manipulation-rule) Ognuno di questi attributi è un valore stringa. La prima regola contiene un'espressione regolare che rappresenta il criterio di corrispondenza. La seconda regola contiene un'espressione regolare che rappresenta il testo di sostituzione. È anche necessario creare un [attributo Manipulation-Target.](/windows/desktop/Nps/sdo-manipulation-target) Questo attributo è un'enumerazione che specifica quale parte delle informazioni dell'utente modificare.

L'ordine in cui vengono creati gli attributi è importante. Server dei criteri di rete elabora gli attributi nell'ordine in cui sono stati creati.

La tabella seguente illustra un esempio di un set di attributi di manipolazione.



| Nome                 | Tipo         | Valore stringa     |
|----------------------|--------------|------------------|
| msManipulationRule   | **VT \_ BSTR** | "@company.com"   |
| msManipulationRule   | **VT \_ BSTR** | "@microsoft.com" |
| msManipulationRule   | **VT \_ BSTR** | "^.+@"           |
| msManipulationRule   | **VT \_ BSTR** | "guest@"         |
| msManipulationTarget | **VT \_ I4**   | "1"              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gerarchia del modello a oggetti](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Attributi supportati SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Creazione di un criterio di richiesta di connessione](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**PROPRIETÀ IAS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 