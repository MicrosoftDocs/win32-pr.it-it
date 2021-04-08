---
description: Impostazioni locali personalizzate
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Impostazioni locali personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50108750fb1209aa210b04d8be9adcd48e5fd308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968322"
---
# <a name="custom-locales"></a>Impostazioni locali personalizzate

**Windows Vista e versioni successive:** Le impostazioni locali personalizzate supportano le proprietà internazionali offrendo un'esperienza utente più appropriata per la cultura rispetto a quelle fornite con le impostazioni locali standard fornite da Microsoft con il sistema operativo. L'utilizzo di impostazioni locali personalizzate consente agli amministratori di estendere il set di impostazioni locali fornito da Microsoft o di sostituire i dati nelle impostazioni locali fornite con Windows, ad esempio i simboli di valuta o i nomi dei mesi dell'anno.

I due tipi di impostazioni locali personalizzate sono le impostazioni locali supplementari e le impostazioni locali di sostituzione. Le impostazioni locali aggiuntive sono impostazioni locali personalizzate che consentono a società, Università, governi e altre terze parti di creare dati sulle impostazioni locali non disponibili nel sistema operativo di spedizione. Le impostazioni locali di sostituzione sono impostazioni locali personalizzate fornite con il sistema operativo senza modificare gli [identificatori delle impostazioni locali](locale-identifiers.md) o [i nomi delle impostazioni locali](locale-names.md).

Per compilare impostazioni locali personalizzate, è possibile usare l'utilità del compilatore delle impostazioni locali fornita da NLS. Per altre informazioni, vedere [Generatore di impostazioni locali Microsoft](https://www.microsoft.com/download/details.aspx?id=41158). Le istruzioni per l'uso delle impostazioni locali personalizzate nelle applicazioni sono disponibili in uso [di impostazioni locali personalizzate](working-with-custom-locales.md).

## <a name="comparison-of-custom-locale-types"></a>Confronto tra tipi di impostazioni locali personalizzati

Nella tabella seguente vengono descritte le differenze tra le impostazioni locali aggiuntive e di sostituzione.



| Elemento                                                                                                                           | Impostazioni locali aggiuntive                                                                                                                                                                                                                   | Impostazioni locali sostitutive                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendari                                                                                                                      | Può includere qualsiasi calendario fornito da Microsoft. Almeno uno dei calendari specificati deve essere il calendario localizzato gregoriano.                                                                                              | Può includere qualsiasi calendario fornito da Microsoft. Almeno uno dei calendari specificati deve essere il calendario localizzato gregoriano e la raccolta deve includere il calendario predefinito delle impostazioni locali sostituite. |
| Ordinamento                                                                                                                        | Può utilizzare uno qualsiasi degli ordinamenti forniti da Microsoft.                                                                                                                                                                                          | Mantiene il comportamento di ordinamento delle impostazioni locali da sostituire.                                                                                                                                                            |
| Nomi di giorno e mese                                                                                                            | Può essere personalizzato solo per il calendario gregoriano standard, non per i calendari non gregoriani e non per i calendari gregoriani specializzati, ad esempio il calendario francese gregoriano Medio Oriente.                                           | Come per le impostazioni locali aggiuntive.                                                                                                                                                                                      |
| Nome della lingua ([impostazioni locali \_ SLANGUAGE](locale-slanguage.md) o [impostazioni locali \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Restituisce le [impostazioni locali \_ SNATIVELANGNAME](locale-snative-constants.md) o [ \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Mantiene il nome della lingua delle impostazioni locali da sostituire.                                                                                                                                                                 |
| Identificatore delle impostazioni locali                                                                                                              | Impostare su [impostazioni locali \_ personalizzate non \_ specificate](locale-custom-constants.md) , a meno che le impostazioni locali non siano gli standard e i formati attualmente selezionati dell'utente, nel qual caso è impostato su impostazioni locali [ \_ personalizzate \_ predefinite](locale-custom-constants.md). | Mantiene l'identificatore delle impostazioni locali che viene sostituito.                                                                                                                                                             |
| Nome delle impostazioni locali                                                                                                                    | Arbitrario deve adattarsi al modello descritto in [nomi delle impostazioni locali](locale-names.md).                                                                                                                                                      | Mantiene il nome delle impostazioni locali da sostituire.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Esempi di impostazioni locali supplementari



| Nome delle impostazioni locali    | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricat | Fabricat è un produttore di computer canadesi con uffici in tutto il mondo. Per garantire un comportamento coerente dell'interfaccia utente per tutti i computer, l'azienda sviluppa le impostazioni locali per l'uso dell'intera azienda.                                                                                                                                                          |
| fr-US          | Woodlawn Bank utilizza Windows XP Embedded per i propri bancomat (Automatic Teller Machine), che la banca si basa su America del Nord con le interfacce utente in francese, inglese e spagnolo. Per garantire un'esperienza coerente, la Banca crea le impostazioni locali per il francese nel Stati Uniti con formati Stati Uniti ma i nomi dei giorni e dei mesi in francese. |



 

## <a name="replacement-locale-example"></a>Esempio di impostazioni locali sostitutive



| Nome delle impostazioni locali | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-US       | Fabricat è un produttore di computer canadesi con uffici in tutto il mondo. Per garantire un comportamento coerente dell'interfaccia utente per tutti i computer, l'azienda sviluppa le impostazioni locali per l'uso dell'intera azienda. Usa un formato a 24 ore, ma in caso contrario funziona come le impostazioni locali supportate per la lingua inglese (Stati Uniti). Poiché le impostazioni locali personalizzate sono così simili alle impostazioni locali supportate, fabricat decide di implementarlo come impostazioni locali sostitutive anziché come impostazioni locali aggiuntive. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Utilizzo di impostazioni locali personalizzate](working-with-custom-locales.md)
</dt> </dl>

 

 



