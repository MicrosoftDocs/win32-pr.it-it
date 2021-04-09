---
description: Il metodo GetSPRM Recupera il registro dei parametri di sistema specificato.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Metodo GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965474"
---
# <a name="getsprm-method"></a>Metodo GetSPRM

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetSPRM` metodo recupera il registro dei parametri di sistema specificato.

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Specifica il registro di cui si desidera recuperare il valore come Integer. Il valore integer deve essere compreso tra 0 e 23.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il contenuto del registro specificato.

## <a name="remarks"></a>Commenti

Il disco controlla i registri dei parametri di sistema (SPRMs). Un'applicazione del lettore non deve accedere a questi registri per le funzionalità di navigazione standard. SPRMs rappresenta lo stato del lettore. Ognuno ha un significato, impostato in base alle preferenze dell'utente, ai comandi del disco e ad altre occorrenze che un'applicazione non ha controllo diretto. Un'applicazione può leggere questi registri ma non scriverli. Per utilizzare i registri in modo efficace, probabilmente sarà necessaria una conoscenza più approfondita dei comandi di spostamento del DVD rispetto a quanto specificato in questa documentazione. Nella tabella seguente viene illustrato il contenuto di ogni registro. Per informazioni più dettagliate sul contenuto del registro, vedere [ **IDvdInfo2:: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Registrazione | Contenuto                        |
|----------|---------------------------------|
| 0        | Codice lingua menu              |
| 1        | Numero flusso audio             |
| 2        | Numero di flusso di immagini subimmagine        |
| 3        | Numero angolo corrente            |
| 4        | Numero del titolo corrente            |
| 5        | Numero titolo                    |
| 6        | Numero PGC                      |
| 7        | Numero del capitolo corrente (PTT)    |
| 8        | Numero pulsante evidenziato       |
| 9        | Timer di spostamento                |
| 10       | Salto PGC per NAV. timer         |
| 11       | Modalità presentazione audio karaoke |
| 12       | Codice di paese/area geografica PML         |
| 13       | PML                             |
| 14       | Impostazione video                   |
| 15       | Funzionalità audio                |
| 16       | Lingua audio                  |
| 17       | Estensione del linguaggio audio        |
| 18       | Lingua di immagine             |
| 19       | Estensione della lingua di immagine   |
| 20       | Codice area del lettore              |
| 21       | Riservato                        |
| 22       | Riservato                        |
| 23       | Riservato                        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



