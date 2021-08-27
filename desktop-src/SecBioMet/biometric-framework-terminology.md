---
title: Terminologia del framework biometrico
description: I termini seguenti vengono usati nella documentazione dell'API Windows Biometric Framework.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd88fe552d9a53d8bcf214280e5b15a9206532383afa87bfee6fe6dd95c9c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127261"
---
# <a name="biometric-framework-terminology"></a>Terminologia del framework biometrico

I termini seguenti vengono usati nella documentazione dell'API Windows Biometric Framework.



| Termine                                                 | Definizione                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Biometric Framework (WBF)<br/>         | Un'architettura del framework in Windows che offre un'interfaccia di gestione coerente e un'esperienza utente per i dispositivi biometrici.<br/>                                                                                                                         |
| Servizio di biometria Windows<br/>                 | Servizio con privilegi che gestisce tutti i dispositivi biometrici usando Windows di dispositivo conformi a Biometric Driver Interface (WBDI).<br/>                                                                                                                   |
| Windows Interfaccia del driver biometrico<br/>        | Uno standard di interfaccia per i driver che gestiscono i sensori di impronta digitale.<br/>                                                                                                                                                                                     |
| Windows Provider di servizi biometrici (WBSP)<br/> | Componente del servizio biometrico Windows che gestisce una categoria specifica di tecnologia biometrica, ad esempio un lettore di impronte digitali. I WBSP sono incorporati nel Windows biometrico. Non sono plug-in e i BSP di terze parti non sono supportati. <br/> |
| Fattore biometrico<br/>                          | Caratteristica personale che può essere misurata e usata per l'identificazione. Ad esempio, le impronte digitali e la geometria della mano.<br/>                                                                                                                           |
| Fattore secondario biometrico<br/>                      | Caratteristica qualificante che può essere usata per definire ulteriormente un fattore biometrico. Ad esempio, per identificare completamente un'impronta digitale (fattore biometrico) è necessario specificare da quale dito proveniva l'impronta (sotto-fattore biometrico).<br/>             |
| Esempio biometrico<br/>                          | Dati risultanti dalla misurazione di una singola caratteristica da un singolo utente, ad esempio l'immagine di un'impronta digitale.<br/>                                                                                                              |
| Modello biometrico<br/>                        | Media statistica generata raccogliendo più campioni biometrici di una singola caratteristica per un singolo utente. Un modello contiene in genere solo le funzionalità necessarie per determinare se un nuovo esempio corrisponde.<br/>             |
| Unità biometrica<br/>                            | Oggetto software che rappresenta un dispositivo biometrico e può essere usato per acquisire ed elaborare campioni biometrici e creare, salvare e associare modelli biometrici.<br/>                                                                                         |
| Adattatore sensore<br/>                            | Componente plug-in unità biometrica che fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di campioni e il controllo del flusso dei dati biometrici all'adattatore del motore.<br/>                                                                 |
| Adattatore motore<br/>                            | Componente plug-in unità biometrica che elabora un campione normalizzando i dati, estraendo caratteristiche e abbinando i dati di esempio ai modelli esistenti.<br/>                                                                                                   |
| Adattatore di archiviazione<br/>                           | Componente plug-in unità biometrico che archivia, gestisce e recupera i modelli.<br/>                                                                                                                                                                      |
| Record di informazioni biometriche (BIR)<br/>        | Struttura di dati che contiene informazioni biometriche non elaborate o elaborate.<br/>                                                                                                                                                                                 |
| Pool di sensori<br/>                               | Raccolta di unità biometriche che condividono criteri di gestione comuni.<br/>                                                                                                                                                                                 |
| Test di attività<br/>                          | Processo che verifica che un campione biometrico non venga falsificato o riprodotto da un campione raccolto in precedenza.<br/>                                                                                                                          |



 

 

 





