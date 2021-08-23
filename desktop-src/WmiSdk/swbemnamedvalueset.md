---
description: Un oggetto SWbemNamedValueSet è una raccolta di oggetti SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Oggetto SWbemNamedValueSet (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdcc3ba2bde6dfdfd0cc732e4376ceb69ba60904f4d787d9030299c248ebb62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732671"
---
# <a name="swbemnamedvalueset-object"></a>Oggetto SWbemNamedValueSet

Un **oggetto SWbemNamedValueSet** è una raccolta di [**oggetti SWbemNamedValue.**](swbemnamedvalue.md) I metodi e le proprietà **di SWbemNamedValueSet** vengono usati principalmente per inviare ulteriori informazioni ai provider quando si inviano determinate chiamate a WMI. Tutte le chiamate in [**SWbemServices**](swbemservices.md)e alcune chiamate in [**SWbemObject**](swbemobject.md)accettano un parametro facoltativo che è un oggetto di questo tipo. Un client può aggiungere informazioni a un **oggetto SWbemNamedValueSet** e inviare l'oggetto **SWbemNamedValueSet** con la chiamata come uno dei parametri. Questo oggetto può essere creato dalla chiamata **CREATEObject** di VBScript.

Per altre informazioni, vedere [Accesso a una raccolta.](accessing-a-collection.md)

> [!Note]  
> Importante: se possibile, non usare questo meccanismo perché può interrompere il modello di accesso uniforme alla base di WMI. Se un provider usa questo meccanismo, è importante che questo meccanismo sia utilizzato il più possibile con moderamento. Se un provider richiede una grande quantità di informazioni di contesto altamente specifiche per rispondere a una richiesta, tutti i client devono essere codificati per fornire queste informazioni. Questo meccanismo consente di accedere a tali provider, se necessario.

 

Un **oggetto SWbemNamedValueSet** è una raccolta di [**elementi SWbemNamedValue.**](swbemnamedvalue.md) Questi elementi vengono aggiunti alla raccolta usando il [**metodo SWbemNamedValueSet.Add.**](swbemnamedvalueset-add.md) Vengono rimossi usando il [**metodo SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) e recuperati usando il [**metodo SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) È possibile accedere ai metodi per inserire qualsiasi informazione di contesto richiesta da un provider dinamico. Dopo aver chiamato uno dei metodi [**SWbemServices,**](swbemservices.md) è possibile riutilizzare **l'oggetto SWbemNamedValueSet** per un'altra chiamata.

Il provider sottostante determina le informazioni contenute in un **oggetto SWbemNamedValueSet.** WMI non usa le informazioni, ma le inoltra semplicemente al provider. I provider devono pubblicare le informazioni di contesto necessarie per il servizio delle richieste.

## <a name="members"></a>Membri

**L'oggetto SWbemNamedValueSet** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemNamedValueSet** dispone di questi metodi.



| Metodo                                            | Descrizione                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](swbemnamedvalueset-add.md)             | Aggiunge un [**oggetto SWbemNamedValue**](swbemnamedvalue.md) alla raccolta.<br/>                                                  |
| [**Clone**](swbemnamedvalueset-clone.md)         | Crea una copia di questa **raccolta SWbemNamedValueSet.**<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Rimuove tutti gli elementi dalla raccolta, rendendo vuoto **l'oggetto SWbemNamedValueSet.**<br/>                                        |
| [**Elemento**](swbemnamedvalueset-item.md)           | Recupera un [**oggetto SWbemNamedValue**](swbemnamedvalue.md) dalla raccolta. Si tratta del metodo predefinito dell'oggetto .<br/> |
| [**Rimuovi**](swbemnamedvalueset-remove.md)       | Rimuove un [**oggetto SWbemNamedValue**](swbemnamedvalue.md) dalla raccolta.<br/>                                             |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemNamedValueSet** ha queste proprietà.



| Proprietà                                             | Tipo di accesso          | Descrizione                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Conteggio**](swbemnamedvalueset-count.md)<br/> | Sola lettura<br/> | Numero di elementi nella raccolta.<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene illustrata la manipolazione di set di valori denominati, nel caso in cui il valore denominato sia un tipo di matrice.


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



Nell'esempio Perl seguente viene illustrata la manipolazione di set di valori denominati, nel caso in cui il valore denominato sia un tipo di matrice.


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




