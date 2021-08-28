---
description: 'Altre informazioni su: Costanti handle non valide'
title: Costanti handle non valide
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: 28a52b2fc7a51572cc7bb78ad7631df41438310a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473277"
---
# <a name="invalid-handle-constants"></a>Costanti handle non valide


_**Si applica a:** Windows | Windows Server_

## <a name="invalid-handle-constants"></a>Costanti handle non valide

Le costanti seguenti indicano handle non validi per diversi aspetti di ESE.


| <p>Costante/valore</p> | <p>Descrizione</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br />(~(JET_INSTANCE)0)</p> | <p>Handle non valido per un'istanza di database.<br /><strong>Windows XP:</strong> Introdotto in Windows XP.</p> | 
| <p>JET_sesidNil<br />(~(JET_SESID)0)</p> | <p>Handle non valido per un ID sessione.</p> | 
| <p>JET_tableidNil<br />(~(JET_TABLEID)0)</p> | <p>Handle non valido per un ID tabella.</p> | 
| <p>JET_bitNil<br />((JET_GRBIT)0)</p> | <p>Handle non valido per un gruppo di bit.</p> | 
| <p>JET_LSNil<br />(~(JET_LS)0)</p> | <p>Handle non valido per l'Archiviazione.</p> | 
| <p>JET_dbidNil<br />((JET_DBID) 0xFFFFFFFF)</p> | <p>Handle non valido per l'ID database.</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


