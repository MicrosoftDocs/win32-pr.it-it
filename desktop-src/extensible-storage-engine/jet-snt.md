---
description: 'Altre informazioni su: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 250ad992ec26b218bab21691f26c0938b6be6921
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481387"
---
# <a name="jet_snt"></a>JET_SNT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

Il [JET_SNT]() di costanti descrive i punti di avanzamento di un'operazione sulle informazioni richieste in una chiamata alla funzione [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) di callback.


| <p>Costante/valore</p> | <p>Descrizione</p> | 
|-----------------------|--------------------|
| <p>JET_sntBegin<br />5</p> | <p>Inizio di un'operazione</p> | 
| <p>JET_sntRequirements<br />7</p> | <p>Non supportata.</p><p><strong>Windows 2000 Server:</strong>  L'operazione viene avviata. In questo caso, l'ultimo parametro della funzione di callback deve essere un puntatore valido a una <a href="gg269328(v=exchg.10).md">struttura JET_SNPROG</a> che indica il numero totale di unità da eseguire.</p> | 
| <p>JET_sntProgress<br />0</p> | <p>Numero di unità completate e numero di unità ancora da completare. Queste informazioni vengono restituite nei membri di una <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> struttura .</p> | 
| <p>JET_sntComplete<br />6</p> | <p>Completamento di un'operazione.</p> | 
| <p>JET_sntFail<br />3</p> | <p>Errore di un'operazione.</p> | 
| <p>JET_sntRecoveryStep<br />8</p> | <p>Controllo del ripristino di un'operazione.</p><div class="alert">&gt; [!NOTE]&gt; <P>Questo valore non è applicabile alle versioni del Windows operativo a partire da Windows 8.</P></div> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
