---
description: Il metodo DVDAdm.ChangePassword salva una nuova password dell'applicazione nel Registro di sistema.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: Metodo ChangePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f5d15eef943afa019f1b1bba4e3b1412978bc5dd8f52f411c504e880428848a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999331"
---
# <a name="changepassword-method"></a>Metodo ChangePassword

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.ChangePassword` metodo salva una nuova password dell'applicazione nel Registro di sistema.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica il nome di accesso dell'utente corrente come stringa. L'oggetto MSDVDAdm ignora questo parametro. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Venduto*
</dt> <dd>

Specifica la vecchia password dell'utente come stringa.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Specifica la nuova password dell'utente come stringa. Non può essere una stringa vuota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Attualmente, il *parametro sUserName* viene ignorato in questo e in tutti i metodi correlati. Ciò significa che chiunque conosca la password può impostare il livello di genitori. Per l'applicazione sono disponibili una sola password e un livello di genitori. Non è disponibile alcun supporto per i singoli nomi di accesso utente o per la gestione di più password. Per applicare i livelli di gestione dei genitori, i genitori devono impostare la password e quindi impostare il livello di genitori appropriato per i membri più piccoli del gruppo di familiari. Quando i genitori vogliono visualizzare un disco con contenuto valutato per adulti, possono modificare il livello e quindi modificarlo al termine della visualizzazione. Finché gli elementi figlio non conoscono la password, possono guardare il contenuto solo a un livello inferiore o inferiore a quello impostato per loro.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



