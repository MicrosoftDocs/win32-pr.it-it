---
description: L'interfaccia IWordInfo è un componente di risorse del linguaggio specifico per il giapponese. L'oggetto analizza il testo e identifica le singole parole, restituendo le parole nella stringa o restituisce le forme del dizionario (radice) delle parole nel testo della stringa.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interfaccia IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522977"
---
# <a name="iwordinfo-interface"></a>Interfaccia IWordInfo

\[Questa interfaccia è obsoleta e non è supportata in Windows Vista.\]

L'interfaccia **IWordInfo** è un componente di risorse del linguaggio specifico per il giapponese. L'oggetto analizza il testo e identifica le singole parole, restituendo le parole nella stringa o restituisce le forme del dizionario (radice) delle parole nel testo della stringa.

## <a name="members"></a>Membri

L'interfaccia **IWordInfo** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordInfo** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWordInfo** dispone di questi metodi.



| Metodo        | Descrizione                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analizza il testo per identificare le parole e fornisce i risultati all'oggetto [WordSink](/previous-versions//ms691570(v=vs.85)) .<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia viene utilizzata per recuperare le interruzioni di parola giapponesi o i form del dizionario per il testo da analizzare. Il formato del dizionario di una parola è il formato uninflected della parola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
