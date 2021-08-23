---
description: ICE74 verifica che la proprietà FASTOEM non sia stata modificata nella tabella Proprietà.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3120b0f4cd40acc53a1bcd3623dac33941a7f5da39bc538781e4ffd1d56345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328321"
---
# <a name="ice74"></a>ICE74

ICE74 verifica che la [**proprietà FASTOEM**](fastoem.md) non sia stata modificata nella [tabella Delle proprietà](property-table.md).

La [**proprietà FASTOEM**](fastoem.md) consente agli OEM di ridurre il tempo necessario per installare le Windows installer per la prima volta. Non può essere usato dopo la prima installazione. Non è necessario creare la proprietà **FASTOEM** nella tabella Property perché questo interferisce con le installazioni successive per la manutenzione, la rimozione o il ripristino dell'applicazione.

ICE74 verifica anche che la [**proprietà UpgradeCode**](upgradecode.md) sia stata modificata nella tabella [Property](property-table.md)e che il relativo valore non sia un GUID Null, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Risultato

ICE74 può inviare gli errori seguenti.



| Errore ICE74                                                                       | Descrizione                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Non è possibile creare la proprietà [**FASTOEM**](fastoem.md) nella tabella Property. | La [**proprietà FASTOEM**](fastoem.md) è stata impostata nella tabella Proprietà.                             |
| ' \[ 2 \] ' non è un [**UpgradeCode valido.**](upgradecode.md)                        | È stato immesso un GUID null per la [**proprietà UpgradeCode**](upgradecode.md) nella tabella Proprietà. |



 

ICE74 può pubblicare l'avviso seguente.



| Avviso ICE74                                                                                                                                                                                             | Descrizione                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| La [**proprietà UpgradeCode**](upgradecode.md) non viene specificata nella tabella Property. È consigliabile che gli autori di pacchetti di installazione specificano **un codice di aggiornamento** per l'applicazione. | La [**proprietà UpgradeCode**](upgradecode.md) non viene specificata nella tabella Property. |



 

## <a name="example"></a>Esempio

ICE74 segnala l'errore seguente se la [**proprietà FASTOEM**](fastoem.md) è impostata: FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà                   | Valore |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Per correggere questo errore, rimuovere [**la proprietà FASTOEM**](fastoem.md) dalla tabella delle proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**FastOEM - proprietà**](fastoem.md)
</dt> <dt>

[Tabella delle proprietà](property-table.md)
</dt> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



