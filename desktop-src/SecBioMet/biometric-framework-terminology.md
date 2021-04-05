---
title: Terminologia di Framework biometrico
description: I termini seguenti vengono usati in tutta la documentazione dell'API Windows Biometric Framework.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f150a30915a44dbd59a5a703577e79dc48933f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713447"
---
# <a name="biometric-framework-terminology"></a>Terminologia di Framework biometrico

I termini seguenti vengono usati in tutta la documentazione dell'API Windows Biometric Framework.



| Termine                                                 | Definizione                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Biometric Framework (WBF)<br/>         | Architettura del Framework in Windows che offre un'interfaccia di gestione coerente e un'esperienza utente per i dispositivi biometrici.<br/>                                                                                                                         |
| Servizio di biometria Windows<br/>                 | Servizio con privilegi che gestisce tutti i dispositivi biometrici usando i driver di dispositivo conformi a WBDI (Windows Biometric Driver Interface).<br/>                                                                                                                   |
| Interfaccia del driver biometrico di Windows<br/>        | Standard di interfaccia per i driver che gestiscono i sensori di impronta digitale.<br/>                                                                                                                                                                                     |
| Provider di servizi biometrici di Windows (WBSP)<br/> | Componente del servizio biometrico di Windows che gestisce una categoria specifica di tecnologia biometrica, ad esempio un lettore di impronte digitali. WBSPs sono incorporati nel servizio biometrico di Windows. Non sono plug-in e i BSP di terze parti non sono supportati. <br/> |
| Fattore biometrico<br/>                          | Caratteristica personale che può essere misurata e usata per l'identificazione. Gli esempi includono le impronte digitali e la geometria manuale.<br/>                                                                                                                           |
| Sottofattore biometrico<br/>                      | Caratteristica idonea che può essere usata per definire ulteriormente un fattore biometrico. Per identificare completamente un'impronta digitale (fattore biometrico), ad esempio, è necessario specificare il dito da cui proviene la stampa (Sottofattore biometrico).<br/>             |
| Esempio di biometrico<br/>                          | Dati che risultano dalla misurazione di una singola caratteristica da un singolo utente, ad esempio l'immagine di un'impronta digitale.<br/>                                                                                                              |
| Modello biometrico<br/>                        | Media statistica generata raccogliendo più campioni biometrici di una singola caratteristica per un singolo utente. Un modello contiene in genere solo le funzionalità necessarie per determinare se un nuovo campione corrisponde.<br/>             |
| Unità biometrica<br/>                            | Un oggetto software che rappresenta un dispositivo biometrico e può essere usato per acquisire ed elaborare esempi biometrici e creare, salvare e abbinare modelli biometrici.<br/>                                                                                         |
| Adattatore sensore<br/>                            | Componente plug-in di unità biometrica che fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di esempi e il controllo del flusso di dati biometrici nell'adattatore del motore.<br/>                                                                 |
| Adattatore motore<br/>                            | Componente plug-in di unità biometrica che elabora un esempio normalizzando i dati, estraendo le funzionalità e associando i dati di esempio ai modelli esistenti.<br/>                                                                                                   |
| Adattatore di archiviazione<br/>                           | Componente plug-in di unità biometrica che archivia, gestisce e recupera i modelli.<br/>                                                                                                                                                                      |
| Record di informazioni biometriche (BIR)<br/>        | Una struttura di dati che contiene informazioni biometriche non elaborate o elaborate.<br/>                                                                                                                                                                                 |
| Pool di sensori<br/>                               | Raccolta di unità biometriche che condividono criteri di gestione comuni.<br/>                                                                                                                                                                                 |
| Test di liveity<br/>                          | Processo che verifica che un campione biometrico non venga falsificato o riprodotto da un campione che è stato precedentemente raccolto.<br/>                                                                                                                          |



 

 

 





