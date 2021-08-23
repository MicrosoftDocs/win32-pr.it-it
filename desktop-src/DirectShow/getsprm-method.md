---
description: Il metodo GetSPRM recupera il registro dei parametri di sistema specificato.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Metodo GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e254d23f0d70890516bc5655f6c4ea38133a8a3733360955cabf9040207f3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536991"
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

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*Iindex*
</dt> <dd>

Specifica il registro di cui si vuole recuperare il valore come integer. Il valore Integer deve essere compreso tra 0 e 23.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il contenuto del registro specificato.

## <a name="remarks"></a>Commenti

Il disco controlla i registri dei parametri di sistema (SPPM). Un'applicazione lettore non deve accedere a questi registri per qualsiasi funzionalità di navigazione standard. I SPN rappresentano lo stato del lettore. Ognuno ha un significato, impostato in base alle preferenze dell'utente, ai comandi del disco e ad altre occorrenze su cui un'applicazione non ha alcun controllo diretto. Un'applicazione può leggere questi registri, ma non può scrivervi. Per usare questi registri in modo efficace, sarà probabilmente necessaria una conoscenza più dettagliata dei comandi di navigazione dei DVD rispetto a quanto fornito in questa documentazione. La tabella seguente illustra il contenuto di ogni registro. Per informazioni più dettagliate sul contenuto del registro, vedere [ **IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Registrazione | Contenuto                        |
|----------|---------------------------------|
| 0        | Codice lingua menu              |
| 1        | Numero di flusso audio             |
| 2        | Numero di flusso dell'immagine secondaria        |
| 3        | Numero angolo corrente            |
| 4        | Numero titolo corrente            |
| 5        | Numero titolo                    |
| 6        | Numero PGC                      |
| 7        | Numero di capitolo corrente (PTT)    |
| 8        | Numero del pulsante evidenziato       |
| 9        | Timer di navigazione                |
| 10       | Passaggio PGC per lo spostamento. timer         |
| 11       | Modalità presentazione audio audio in formato audio audio |
| 12       | Codice paese/area geografica PML         |
| 13       | Pml                             |
| 14       | Impostazione video                   |
| 15       | Funzionalità audio                |
| 16       | Lingua audio                  |
| 17       | Estensione del linguaggio audio        |
| 18       | Lingua delle immagini secondarie             |
| 19       | Estensione del linguaggio delle immagini secondarie   |
| 20       | Codice dell'area del lettore              |
| 21       | Riservato                        |
| 22       | Riservato                        |
| 23       | Riservato                        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



