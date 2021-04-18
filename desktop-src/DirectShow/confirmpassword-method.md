---
description: Il metodo DVDAdm. ConfirmPassword verifica se la password specificata corrisponde alla password salvata in precedenza.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Metodo ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328827"
---
# <a name="confirmpassword-method"></a>Metodo ConfirmPassword

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.ConfirmPassword` metodo verifica se la password specificata corrisponde alla password salvata in precedenza.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica il nome dell'utente sotto forma di stringa.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Specifica la nuova password sotto forma di stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce true se la password specificata corrisponde alla password esistente; in caso contrario, false.

## <a name="remarks"></a>Commenti

Attualmente, il parametro *sUserName* viene ignorato in questo e in tutti i metodi correlati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




