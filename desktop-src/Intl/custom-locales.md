---
description: Impostazioni locali personalizzate
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Impostazioni locali personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda75d0d097bf6860e1385bb2557d56c2b2d2a1df530404781817590e381b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754921"
---
# <a name="custom-locales"></a>Impostazioni locali personalizzate

**Windows Vista e versioni successive:** Le impostazioni locali personalizzate supportano proprietà internazionali che offrono un'esperienza utente culturalmente appropriata rispetto a quelle fornite con le impostazioni locali standard fornite da Microsoft con il sistema operativo. L'uso di impostazioni locali personalizzate consente agli amministratori di estendere il set di impostazioni locali fornito da Microsoft o di sostituire i dati in impostazioni locali fornite con Windows, ad esempio simboli di valuta o nomi dei mesi dell'anno.

I due tipi di impostazioni locali personalizzate sono le impostazioni locali supplementari e le impostazioni locali di sostituzione. Le impostazioni locali supplementari sono impostazioni locali personalizzate che consentono a società, università, enti governativi e altre terze parti di creare dati sulle impostazioni locali non disponibili nel sistema operativo di spedizione. Le impostazioni locali sostitutive sono impostazioni locali personalizzate disponibili con il sistema operativo senza modificare gli identificatori [delle impostazioni locali o](locale-identifiers.md) i nomi delle impostazioni [locali](locale-names.md).

È possibile usare l'utilità Locale Builder fornita da NLS per compilare impostazioni locali personalizzate. Per altre informazioni, vedere [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). Le istruzioni per l'uso delle impostazioni locali personalizzate nelle applicazioni sono disponibili in [Uso delle impostazioni locali personalizzate](working-with-custom-locales.md).

## <a name="comparison-of-custom-locale-types"></a>Confronto dei tipi di impostazioni locali personalizzati

Nella tabella seguente vengono descritte le differenze tra le impostazioni locali supplementari e le impostazioni locali di sostituzione.



| Elemento                                                                                                                           | Impostazioni locali supplementari                                                                                                                                                                                                                   | Impostazioni locali di sostituzione                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendari                                                                                                                      | Può includere qualsiasi calendario fornito da Microsoft. Almeno uno dei calendari forniti deve essere il calendario gregoriano localizzato.                                                                                              | Può includere qualsiasi calendario fornito da Microsoft. Almeno uno dei calendari specificati deve essere il calendario gregoriano localizzato e la raccolta deve includere il calendario predefinito delle impostazioni locali sostituite. |
| Ordinamento                                                                                                                        | Può usare qualsiasi ordinamento fornito da Microsoft.                                                                                                                                                                                          | Mantiene il comportamento di ordinamento delle impostazioni locali da sostituire.                                                                                                                                                            |
| Nomi di giorno e mese                                                                                                            | Può essere personalizzato solo per il calendario gregoriano standard, non per i calendari non gregoriani e non per i calendari gregoriani specializzati, ad esempio il calendario gregoriano medio-orientale francese.                                           | Come per le impostazioni locali supplementari.                                                                                                                                                                                      |
| Nome della lingua ([LOCALE \_ SLANGUAGE](locale-slanguage.md) o [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Restituisce [LOCALE \_ SNATIVELANGNAME o](locale-snative-constants.md) LOCALE [ \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Mantiene il nome della lingua delle impostazioni locali da sostituire.                                                                                                                                                                 |
| Identificatore delle impostazioni locali                                                                                                              | Impostare su [LOCALE \_ CUSTOM \_ UNSPECIFIED](locale-custom-constants.md) a meno che le impostazioni locali non siano le impostazioni locali attualmente selezionate dall'utente standard e formati, nel qual caso è impostato su [IMPOSTAZIONI LOCALI CUSTOM \_ \_ DEFAULT](locale-custom-constants.md). | Mantiene l'identificatore delle impostazioni locali delle impostazioni locali da sostituire.                                                                                                                                                             |
| Nome delle impostazioni locali                                                                                                                    | Arbitrario; deve essere in base al modello descritto in [Nomi delle impostazioni locali](locale-names.md).                                                                                                                                                      | Mantiene il nome delle impostazioni locali delle impostazioni locali da sostituire.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Esempi di impostazioni locali supplementari



| Nome delle impostazioni locali    | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricam | Fabricam è un produttore di PC canadese con uffici in tutto il mondo. Per garantire un comportamento coerente dell'interfaccia utente per tutti i computer, l'azienda sviluppa impostazioni locali per l'uso a livello aziendale.                                                                                                                                                          |
| fr-US          | Woodlawn Bank usa Windows XP Embedded per i suoi bancomat automatizzati, che la banca spedisce in tutto il America del Nord con interfacce utente in francese, inglese e spagnolo. Per offrire un'esperienza coerente, la banca crea le impostazioni locali per il francese nel Stati Uniti con formati Stati Uniti ma nomi di giorni e mesi in francese. |



 

## <a name="replacement-locale-example"></a>Esempio di impostazioni locali di sostituzione



| Nome delle impostazioni locali | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-US       | Fabricam è un produttore di PC canadese con uffici in tutto il mondo. Per garantire un comportamento coerente dell'interfaccia utente per tutti i computer, l'azienda sviluppa impostazioni locali per l'uso a livello aziendale. Usa un orologio a 24 ore, ma in caso contrario si comporta come le impostazioni locali supportate per la lingua inglese (Stati Uniti). Poiché le impostazioni locali personalizzate sono così simili alle impostazioni locali supportate, Fabricam decide di implementarla come impostazioni locali sostitutive anziché come impostazioni locali supplementari. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Uso delle impostazioni locali personalizzate](working-with-custom-locales.md)
</dt> </dl>

 

 



